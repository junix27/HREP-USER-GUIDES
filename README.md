# Dynamic Template Generator Implementation Guide

## 1. Database Structure

### Templates Table
```sql
DROP TABLE IF EXISTS templates CASCADE;
CREATE TABLE IF NOT EXISTS templates (
    template_id SERIAL PRIMARY KEY,
    template_name varchar(100) NOT NULL,
    template_schema jsonb NOT NULL,
    is_default BOOLEAN default false, -- set to true if the template is the default template
    CONSTRAINT unq_template_name UNIQUE (template_name)
);

-- If you will be using multiple templates, you can create a table where you can fetch the corresponding template: 

DROP TABLE IF EXISTS record_format CASCADE;
CREATE TABLE IF NOT EXISTS record_format(
    format_id SERIAL PRIMARY KEY,
    format_name VARCHAR(100),
    template_id INTEGER
);

```

### Template Values Table
```sql
DROP TABLE IF EXISTS template_values CASCADE;
CREATE TABLE IF NOT EXISTS template_values (
    value_id SERIAL PRIMARY KEY,
    record_id integer NOT NULL, -- The primary key referenced on your main records table
    template_id integer NOT NULL,
    values jsonb NOT NULL,
    created_by integer,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_by integer,
    updated_at TIMESTAMP
);


```

### Main Table Example
```sql
    DROP TABLE IF EXISTS records CASCADE;
    CREATE TABLE IF NOT EXISTS records(
        record_id SERIAL PRIMARY KEY,
        record_format_id INTEGER,
        record_title VARCHAR(100),
        -- Add other fields necessary
    )
```

### Indexing 
**Add Necessary Indexes Depending on use case**
```sql
DROP INDEX IF EXISTS idx_template_values;
DROP INDEX IF EXISTS idx_template_values ON template_values(record_id);
```

## 2. Template Schema Structure

### Basic Structure
```json
{
    "1.0": {  // Section code
        "code": "1.0",
        "name": "Section Name",
        "description": "Section description",
        "fields": [
            {
                "code": "1.1",
                "name": "Field Name",
                "type": "text",
                "required": true,
                "options": {},
                "help": "Helper text",
                "mapping": {},
                "conditional": {}
            }
        ]
    }
}
```

### Field Properties Explained

1. **Core Properties**
```json
{
    "code": "1.1",        // Unique field identifier
    "name": "Title",      // Display name
    "type": "text",       // Field type
    "required": true      // Mandatory flag
}
```

2. **Field Options**
```json
{
    "options": {
        "maxLength": 500,     // For text fields
        "rows": 4,           // For textarea
        "min": 0,           // For numbers
        "max": 100,         // For numbers
        "step": 1,          // For numbers
        "values": [         // For select/radio
            {
                "label": "Option 1",
                "value": "1"
            }
        ]
    }
}
```

3. **Database Mapping**
```json
{
    "mapping": {
        "source": "records",           // Source table
        "field": "record_title",         // Database field
        "lookup": {                  // For dropdowns lookup on specific tables
            "table": "record_formats",
            "label": "format_name",
            "value": "format_id"
        }
    }
}

// You can ommit values property if you will be using lookup
```

4. **Conditional Display**
```json
{
    "conditional": {
        "field": "1.2",             // Controlling field
        "value": "specific_value",   // Required value of the controlling field
    }
}
```

## 3. Backend Service Implementation (app/lib/RecordsService.php)

### Template Service
```php
<?php
// You can add functions depending on what you need on your project
namespace PHPMaker2024\YOUR_PROJECT\Service;
@session_start();

use PHPMaker2024\YOUR_PROJECT as App;

class TemplateService {
    
    // Function to get the templates
    public function getTemplates() {
        try {
            $sql = "SELECT template_id, template_name, template_schema, is_default
                    FROM " . App\QuotedName("templates", "DB") . "
                    ORDER BY template_name";
            
            $templates = App\ExecuteRows($sql);
            return ["success" => true, "data" => $templates];
        } catch (\Exception $e) {
            return ["success" => false, "message" => $e->getMessage()];
        }
    }
    
    // Function to get the existing records on your main table and creating template values
    public function getRecord($id) {
        try {
            $sql = "SELECT r.*,
                    rf.template_id as format_template_id
                    FROM " . App\QuotedName("records", "DB") . " r
                    LEFT JOIN " . App\QuotedName("record_format", "DB") . " rf 
                        ON r.record_format_id = rf.format_id
                    WHERE r.record_id = " . App\QuotedValue($id, App\DataType::NUMBER);
            
            $record = App\ExecuteRow($sql);
            //Add  other joins if needed
            
            if (!$record) {
                return ["success" => false, "message" => "Record not found"];
            }
    
            // Check current template values
            $sql = "SELECT v.*, t.template_name, t.template_schema
                    FROM " . App\QuotedName("template_values", "DB") . " v
                    JOIN " . App\QuotedName("templates", "DB") . " t 
                        ON v.template_id = t.template_id
                    WHERE v.record_id = " . App\QuotedValue($id, App\DataType::NUMBER);
    
            $template_records = App\ExecuteRow($sql);
    
            // If no existing template records, create mapped values from your main table (record)
            if (!$template_records) {
                // Get the template
                $sql = "SELECT * FROM " . App\QuotedName("templates", "DB") . "
                        WHERE template_id= ". App\QuotedValue($record["format_template_id"], App\DataType::NUMBER);
                
                $template = App\ExecuteRow($sql);
                if ($template) {
                    // Map record data to template fields
                    $mappedValues = $this->mapRecordToTemplate($record, $template);
                    
                    // Create template record
                    $template_records = [
                        'template_id' => $template['template_id'],
                        'template_name' => $template['template_name'],
                        'template_schema' => $template['template_schema'],
                        'values' => json_encode($mappedValues)
                    ];
    
                    // Save curent template mapped values
                    $this->saveTemplateValues($id, $template['template_id'], $mappedValues);
                }
            }
    
           
    
            return [
                "success" => true,
                "data" => [
                    "record" => $record,
                    "template_records" => $template_records
                ]
            ];
    
        } catch (\Exception $e) {
            return ["success" => false, "message" => $e->getMessage()];
        }
    }

    // Function for saving changes on main table and the template values
    public function saveRecord($data) {
        try {
            App\Execute("BEGIN");
    
            $recordId = $data['record_id']; // Get the id of your main table first
            $userId = App\CurrentUserID();

            // Save template values if provided
            if (isset($data['template_values']) && isset($data['template_id'])) {
                // Get template for mapping
                $template = App\ExecuteRow(
                    "SELECT * FROM " . App\QuotedName("templates", "DB") . 
                    " WHERE template_id = " . App\QuotedValue($data['template_id'], App\DataType::NUMBER)
                );

                if ($template) {
                    // Update mapped fields of the template in the main table if there are changes on the template
                    $this->updateMappedValues($recordId, $data['template_values'], $template);
                    
                    // Save templates values
                    $this->saveTemplateValues($recordId, $data['template_id'], $data['template_values']);
                }
            }
    
            // Update the other fields on the main table not existing in the template

            /* Uncomment this part if you have other fields that you want to update on the main table
                $sql = "UPDATE " . App\QuotedName("records", "DB") . "
                        SET sample_field = " . App\QuotedValue($data['sample_field'], App\DataType::NUMBER) . ",
                            updated_by = " . App\QuotedValue($userId, App\DataType::NUMBER) . ",
                            updated_at = CURRENT_TIMESTAMP
                        WHERE record_id = " . App\QuotedValue($recordId, App\DataType::NUMBER);

                App\Execute($sql);
            */
        
    
            

            // Add other necessary processes and data handling in this section (status logs, audit logs, notification, mailing, etc.)
    
            App\Execute("COMMIT");
            return ["success" => true];
    
        } catch (\Exception $e) {
            App\Execute("ROLLBACK");
            return ["success" => false, "message" => $e->getMessage()];
        }
    }

    // Function to save mapped template values
    public function saveTemplateValues($recordId, $templateId, $values) {
        try {
            // Check if values already exist
            $sql = "SELECT value_id FROM " . App\QuotedName("template_values", "DB") . "
                    WHERE record_id = " . App\QuotedValue($recordId, App\DataType::NUMBER);
            
            $existingId = App\ExecuteScalar($sql);
            
            if ($existingId) {
                // Update existing values
                $sql = "UPDATE " . App\QuotedName("template_values", "DB") . "
                        SET values = " . App\QuotedValue(json_encode($values), App\DataType::STRING) . ",
                            updated_by = " . App\QuotedValue(App\CurrentUserID(), App\DataType::NUMBER) . ",
                            updated_at = CURRENT_TIMESTAMP
                        WHERE record_id = " . App\QuotedValue($recordId, App\DataType::NUMBER);
            } else {
                // Insert new values
                $sql = "INSERT INTO " . App\QuotedName("template_values", "DB") . "
                        (record_id, template_id, values, created_by)
                        VALUES (" .
                        App\QuotedValue($recordId, App\DataType::NUMBER) . "," .
                        App\QuotedValue($templateId, App\DataType::NUMBER) . "," .
                        App\QuotedValue(json_encode($values), App\DataType::STRING) . "," .
                        App\QuotedValue(App\CurrentUserID(), App\DataType::NUMBER) . ")";
            }

            App\Execute($sql);
            return ["success" => true];

        } catch (\Exception $e) {
            return ["success" => false, "message" => $e->getMessage()];
        }
    }

    //Function to update mapped values
    private function updateMappedValues($recordId, $templateValues, $template) {
        try {
            if (!$templateValues || !$template) return;
    
            $schema = json_decode($template['template_schema'], true);
            $updateFields = [];
    
            // Collect mapped fields that need updating
            foreach ($schema as $section) {
                if (!isset($section['fields'])) continue;
    
                foreach ($section['fields'] as $field) {
                    if (!isset($field['mapping']) || !isset($field['mapping']['source'])) continue;
    
                    $fieldCode = $field['code'];
                    $recordField = $field['mapping']['field'];
    
                    // Check if value exists and has been modified
                    if (isset($templateValues[$fieldCode]) && 
                        isset($templateValues["{$fieldCode}_modified"]) && 
                        $templateValues["{$fieldCode}_modified"]) {
                        
                        // Handle lookup fields
                        if (isset($field['mapping']['lookup'])) {
                            $updateFields[$recordField] = $templateValues["{$fieldCode}_id"];
                        } else {
                            $updateFields[$recordField] = $templateValues[$fieldCode];
                        }
                    }
                }
            }
    
            // If we have fields to update, construct and execute UPDATE query
            if (!empty($updateFields)) {
                $sets = [];
                foreach ($updateFields as $field => $value) {
                    $sets[] = App\QuotedName($field, "DB") . " = " . 
                             App\QuotedValue($value, App\DataType::STRING);
                }
    
                $sql = "UPDATE " . App\QuotedName("records", "DB") . "
                        SET " . implode(", ", $sets) . ",
                            updated_by = " . App\QuotedValue(App\CurrentUserID(), App\DataType::NUMBER) . ",
                            updated_at = CURRENT_TIMESTAMP
                        WHERE record_id = " . App\QuotedValue($recordId, App\DataType::NUMBER);
    
                App\Execute($sql);
            }
    
            return true;
        } catch (\Exception $e) {
            throw new \Exception("Failed to update mapped fields: " . $e->getMessage());
        }
    }
    
    // Function to map specific records to the template values
    private function mapRecordToTemplate($record, $template) {
        try {
            $mappedValues = [];
            $schema = json_decode($template['template_schema'], true);
    
    
            foreach ($schema as $sectionCode => $section) {
                
                if (!isset($section['fields'])) {
                    continue;
                }
    
                foreach ($section['fields'] as $field) {
                    // If no mapping indicated, continue
                    if (!isset($field['mapping'])) continue;
                    
                    $mapping = $field['mapping'];
                    if (!$mapping['source']) continue; //check if there is a source field for the mapping
    
                    $value = null;
    
                    if (isset($mapping['field']) && isset($record[$mapping['field']])) {
                        $value = $record[$mapping['field']];
                        
                        //for template sections that has lookup, we will fetch the data from that table
                        if (isset($mapping['lookup'])) {
                            $lookupTable = $mapping['lookup']['table'];
                            $lookupKey = $mapping['lookup']['value'];
                            $lookupField = $mapping['lookup']['label'];
                            
                            $lookupId = $value;

                            //Validate first if the table is existing, indicate the schema to be used if you are using bridge from one database to another
                            if ($this->validateLookupTable($lookupTable, "public")) {
                                if ($lookupId) {
                                    $mappedValues[$field['code'] . '_id'] = $lookupId;
                                    $lookupValue = $this->performLookup($lookupTable, $lookupKey, $lookupField, $lookupId);
                                    if ($lookupValue !== null) {
                                        $value = $lookupValue;
                                    }
                                }
                            }
                        }
                    }
    
                    if ($value !== null) {
                        $mappedValues[$field['code']] = $value;
                        $mappedValues[$field['code'] . '_source'] = 'records';
                        $mappedValues[$field['code'] . '_modified'] = false;
                    }
                }
            }
    
            return $mappedValues;
    
        } catch (\Exception $e) {
            return [];
        }
    }

    //Function to validate if the lookup table is existing
    private function validateLookupTable($table, $schema = 'public') {
        try {
            $sql = "SELECT EXISTS (
                SELECT FROM information_schema.tables 
                WHERE table_schema = " . App\QuotedValue(strtolower($schema), App\DataType::STRING) .
                "AND table_name = " . App\QuotedValue(strtolower($table), App\DataType::STRING) . "
            )";
            
            $exists = App\ExecuteScalar($sql);
            
            return $exists;
        } catch (\Exception $e) {
            return false;
        }
    }

    // Function to perform lookup on the table
    private function performLookup($table, $key, $field, $value) {
        if (!$value) return null;
        
        try {
            $sql = "SELECT $field as label
                    FROM " . App\QuotedName($table, "DB") . "
                    WHERE $key = " . App\QuotedValue($value, App\DataType::NUMBER);
            
            $result = App\ExecuteScalar($sql);
            
            return $result;
            
        } catch (\Exception $e) {
            return null;
        }
    }

    // Function to get values from the lookup table
    public function getLookupValues($table, $label, $value) {
        try {
    
            $sql = "SELECT 
                        $value as value,
                        $label as label
                    FROM " . App\QuotedName($table, "DB") . "
                    ORDER BY $label";
    
            $rows = App\ExecuteRows($sql);
            return ["success" => true, "data" => $rows];
            
        } catch (\Exception $e) {
            return ["success" => false, "message" => $e->getMessage()];
        }
    }
}
```
## 4. Backend Routes Implementation (app/api/Records.php)
```php
<?php
// You can add routes depending on what you need on your project
namespace PHPMaker2024\YOUR_PROJECT;
@session_start();

use PHPMaker2024\YOUR_PROJECT\Service\TemplateService;

$templateService = new TemplateService();
// You can declare other services you that you will be using

// Endpoint to save records
$app->post("/records/save", function ($request, $response, $args) use ($templateService) {
    try {
        $data = $request->getParsedBody();
        if (empty($data['record_id'])) {
            return $response->withJson([
                "success" => false,
                "message" => "Record ID is required"
            ]);
        }

        $result = $templateService->saveRecord($data);
        return $response->withJson($result);

    } catch (\Exception $e) {
        return $response->withJson([
            "success" => false,
            "message" => $e->getMessage()
        ]);
    }
})->add($jwtMiddleware);

// Endpoint to get the template(s) to be used
$app->get("/records/templates", function ($request, $response, $args) use ($templateService) {
    $result = $templateService->getTemplates();
    return $response->withJson($result);
})->add($jwtMiddleware);

// Enpoint to save changes on template values
$app->post("/records/{id}/template", function ($request, $response, $args) use ($templateService) {
    try {
        $data = $request->getParsedBody();
        //Check first if the template and values are existing on the request
        if (!isset($data['template_id']) || !isset($data['values'])) {
            return $response->withJson([
                "success" => false,
                "message" => "Template ID and values are required"
            ]);
        }

        $result = $templateService->saveTemplateValues($args['id'], $data['template_id'], $data['values']);
        return $response->withJson($result);

    } catch (\Exception $e) {
        return $response->withJson([
            "success" => false,
            "message" => $e->getMessage()
        ]);
    }
})->add($jwtMiddleware);

// Endpoint for populating select fields with lookup
$app->get("/records/lookup/{table}/{label}/{value}", function ($request, $response, $args) use ($templateService) {
    try {
        $table = $args['table'];
        $label = $args['label'];
        $value = $args['value'];
        $result = $templateService->getLookupValues($table, $label, $value);
        return $response->withJson($result);
    } catch (\Exception $e) {
        return $response->withJson([
            "success" => false,
            "message" => $e->getMessage()
        ]);
    }
})->add($jwtMiddleware);

// Endpoint for fetching the main records
$app->get("/records/{id}", function ($request, $response, $args) use ($templateService) {
    try {
        $result = $templateService->getRecord($args['id']);
        return $response->withJson($result);
    } catch (\Exception $e) {
        return $response->withJson([
            "success" => false,
            "message" => $e->getMessage()
        ]);
    }
})->add($jwtMiddleware);
```

## 5. Frontend Implementation (app/pages/records.php)

### HTML Form
```php
<?php
namespace PHPMaker2024\YOUR_PROJECT;
@session_start();

?>
<style>
    /* Add the styles here  or your can create a css file under YOUR_PROJECT_FOLDER/css/your_folder/your_css.css and link it on the YOUR_PROJECT_FOLDER/app/pages/records.php */
</style>
<div class="container">
    <form id="templateForm" autocomplete="off">
        <div id="templateContainer" class="form-container"></div>
        <div class="button-container d-flex justify-content-end mt-3">
            <button type="submit" id="btnSubmit" class="btn btn-primary">
                <i class="fas fa-save me-2"></i>Save Record
            </button>
        </div>
    </form>
</div>
<script>
    /* Add the script here or your can create a js file under YOUR_PROJECT_FOLDER/js/your_folder/your_js.js and link it on the YOUR_PROJECT_FOLDER/app/pages/records.php */
</script>
```
### Styles
```css
/* Base Layout */
.form-container {
    background-color: white;
    border-radius: 0.5rem;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    padding: 1.5rem;
    margin-bottom: 1.5rem;
    border: 1px solid #e2e8f0;
}

/* Form Controls */
.required-label::after {
    content: "*";
    color: #dc2626;
    margin-left: 0.25rem;
}

.form-control:disabled,
.form-select:disabled {
    background-color: #f8fafc;
    opacity: 0.75;
}

.validation-error {
    color: #dc2626;
    font-size: 0.875rem;
    margin-top: 0.25rem;
    display: block;
}

.is-invalid {
    border-color: #dc2626;
}

/* Section Styling */
.template-section {
    border: 1px solid #e2e8f0;
    border-radius: 0.5rem;
    margin-bottom: 1.5rem;
    overflow: hidden;
}

.template-section-header {
    background-color: #f8fafc;
    padding: 1rem;
    cursor: pointer;
    user-select: none;
    border-bottom: 1px solid #e2e8f0;
    transition: background-color 0.2s;
}

.template-section-header:hover {
    background-color: #f1f5f9;
}

.template-section-title {
    display: flex;
    align-items: baseline;
    gap: 0.5rem;
}

.section-name {
    font-size: 1.125rem;
    font-weight: 600;
    color: #111827;
}

.section-code {
    font-size: 0.875rem;
    color: #6b7280;
}

.template-section-description {
    font-size: 0.875rem;
    color: #6b7280;
    margin-top: 0.25rem;
}

/* Icons */
.fas {
    transition: transform 0.2s ease-in-out;
}

.fa-chevron-up {
    transform: rotate(180deg);
}

.fa-chevron-down {
    transform: rotate(0deg);
}

/* Button Styling */
.btn-primary {
    background-color: #2563eb;
    border-color: #2563eb;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 0.375rem;
    font-weight: 500;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
}

.btn-primary:hover {
    background-color: #1d4ed8;
    border-color: #1d4ed8;
}

.btn-primary:disabled {
    opacity: 0.65;
    cursor: not-allowed;
}

/* Loading Animation */
.fa-spin {
    animation: fa-spin 1s infinite linear;
}

@keyframes fa-spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* Field Container */
.field-container {
    position: relative;
}

.field-container.has-error .form-control,
.field-container.has-error .form-select {
    border-color: #dc2626;
}

.container {
    display: flex;
    flex-direction: column;
    min-height: 100%;
    padding: 1rem;
}

.form-container {
    flex: 1;
}

form#templateForm {
    display: flex;
    flex-direction: column;
    height: 100%;
}

/* Mobile Responsiveness */
@media (max-width: 768px) {
    .form-container {
        padding: 1rem;
    }

    .row {
        margin-right: -0.5rem;
        margin-left: -0.5rem;
    }

    .col-md-3, .col-md-4, .col-md-6 {
        padding-right: 0.5rem;
        padding-left: 0.5rem;
    }
}

/* Add more styles as needed */
```
### Javascript
```javascript
/* This is the default script needed to initialize the template form. Add other scripts depending on your project as needed */

class RecordsForm {
    constructor() {
        // Construct all constants to be used 
        this.mapSource = 'records'; // Change this depending on the source you declared on the template
        this.recordId = this.getRecordIdFromUrl();
        this.formTemplate = null;
        this.recordData = null;
        this.templateValues = null;
        this.apiToken = window.ew?.API_JWT_TOKEN; // Token to be used on function API Calling
        
        this.initialize();
    }
    
    async initialize() {
        try {
            
            // Load main record data first
            await this.loadRecord();

            // Load all reference data in parallel
            await Promise.all([
                // Load the template(s)
                this.loadTemplates()
            ]);

            // Setup form based on loaded data
            this.setupForm();
            this.initializeTooltips();

        } catch (error) {
            this.showError('Failed to initialize form: ' + error.message);
        }
    }

    // Function for event binding
    bindEvents() {
        // Action buttons
        document.getElementById('btnSubmit')?.addEventListener('click', () => this.handleSubmit());

        // Form validation
        document.getElementById('templateForm')?.addEventListener('submit', (e) => {
            e.preventDefault();
            this.handleSubmit();
        });
    }

    // Function to handle form submission
    async handleSubmit() {
        // Clear any existing validation messages first
        this.clearValidationErrors();

        const isValid = this.validateForm();
        
        if (!isValid) {
            // Show error message only if validation fails
            this.showError('Please fill in all required fields.');
            
            // Make sure required fields are highlighted
            document.querySelectorAll('[data-template-field][required]').forEach(field => {
                if (!field.value.trim()) {
                    this.addValidationError(field, 'This field is required');
                }
            });
            
            return;
        }

    const confirmed = await Swal.fire({
        title: 'Confirm Submission',
        text: 'Are you sure you want to submit this record?',
        icon: 'warning',
        showCancelButton: true,
        confirmButtonText: 'Yes, submit',
        cancelButtonText: 'Cancel'
    });

    if (confirmed.isConfirmed) {
        await this.saveRecord();
    }
}

    async saveRecord() {
        const submitBtn = document.getElementById('btnSubmit');
        try {
            // Disable button and show loading state
            submitBtn.disabled = true;
            submitBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i>Saving...';

            const formData = {
                record_id: this.recordId,
                template_id: this.formTemplate.template_id,
                template_values: this.getTemplateValues()
            };

            const result = await this.fetchApi('save', {
                method: 'POST',
                body: JSON.stringify(formData)
            });

            if (result.success) {
                await Swal.fire({
                    icon: 'success',
                    title: 'Success',
                    text: 'Record saved successfully',
                    timer: 2000
                });
                
                await this.loadRecord();
                this.setupForm();
            } else {
                throw new Error(result.message);
            }

        } catch (error) {
            this.showError('Failed to save record: ' + error.message);
        } finally {
            // Restore button state
            submitBtn.disabled = false;
            submitBtn.innerHTML = '<i class="fas fa-save me-2"></i>Save Record';
        }
    }

    // Global Function for API Communication
    async fetchApi(endpoint, options = {}) {
        try {
            const defaultOptions = {
                headers: {
                    'X-Authorization': `Bearer ${this.apiToken}`,
                    'Content-Type': 'application/json'
                }
            };

            const response = await fetch(`api/records/${endpoint}`, { // Replace api/records/ with your corresponding API endpoint
                ...defaultOptions, 
                ...options 
            });
            
            if (!response.ok) {
                throw new Error('API request failed');
            }
            
            const data = await response.json();
            return data;
        } catch (error) {
            console.error('API Error:', error);
            throw error;
        }
    }

    // Main function to load the records
    async loadRecord() {
        try {
            const response = await this.fetchApi(`${this.recordId}`);
            if (!response.success || !response.data) {
                throw new Error('Failed to load record data');
            }

            this.recordData = response.data.record;
            this.templateValues = response.data.template_records;

            // Set template values if they exist
            if (this.templateValues?.values) {
                setTimeout(() => {
                    this.setTemplateValues(this.templateValues.values);
                }, 200);
            }

        } catch (error) {
            throw new Error('Failed to load record: ' + error.message);
        }
    }


    // Function to load the Template(s) available    
    async loadTemplates() {
        try {
            const result = await this.fetchApi('templates');
            console.log('Templates API Response:', result);
            
            if (!result.success || !result.data || result.data.length === 0) {
                console.error('No templates found or invalid template data');
                return;
            }

            if (result.success) {
                // Get template ID from record format (or any table handling the templates)
                const formatTemplateId = this.recordData?.format_template_id;
                console.log('Format template ID:', formatTemplateId); // Debug

                // Find the specified template
                let templateToUse;
                if (formatTemplateId) {
                    templateToUse = result.data.find(t => t.template_id === formatTemplateId);
                }
                
                // Fallback to default template if no template found
                if (!templateToUse) {
                    templateToUse = result.data.find(t => t.is_default === true) || result.data[0];
                }

                console.log('Template to use:', templateToUse); // Debug

                if (templateToUse) {
                    this.formTemplate = templateToUse;
                    await this.createTemplateForm(JSON.parse(templateToUse.template_schema));
                    
                    // Set values if they exist
                    if (this.templateValues?.values) {
                        setTimeout(() => {
                            this.setTemplateValues(this.templateValues.values);
                        }, 100);
                    }
                }
            }
        } catch (error) {
            console.error('Template loading error:', error); // Debug
            throw new Error('Failed to load templates: ' + error.message);
        }
    }

    // Function to populate select options with lookup
    async populateLookupOptions(select, lookupTable, labelField, valueField) {
        try {
            const currentId = select.getAttribute('data-current-value');
            const field = this.findFieldByCode(select.getAttribute('data-template-field'));
            
            const response = await this.fetchApi(`lookup/${lookupTable}/${labelField}/${valueField}`);
            if (!response.success) {
                throw new Error(response.message || 'Failed to load lookup values');
            }

            // Build options HTML
            select.innerHTML = '<option value="">Select...</option>';
            response.data.forEach(item => {
                const option = document.createElement('option');
                option.value = item.value;
                option.textContent = item.label;
                
                // Set selected based on the data-current-value
                if (currentId && item.value.toString() === currentId.toString()) {
                    option.selected = true;
                }
                
                select.appendChild(option);
            });

        } catch (error) {
            console.error('Error loading lookup values:', error);
            select.innerHTML = '<option value="">Error loading options</option>';
        }
    }

    // Function to get template values
    getTemplateValues() {
        const values = {};
        document.querySelectorAll('[data-template-field]').forEach(input => {
            const code = input.getAttribute('data-template-field');
            
            if (input.tagName.toLowerCase() === 'select') {
                const field = this.findFieldByCode(code);
                
                if (field?.mapping?.lookup) {
                    if (input.value) {
                        values[code] = input.options[input.selectedIndex].text;
                        values[`${code}_id`] = input.value;
                        values[`${code}_source`] = this.mapSource;
                        values[`${code}_modified`] = this.templateModifiedFields?.[code] || false;
                    }
                } else {
                    if (input.value.trim()) {
                        values[code] = input.value.trim();
                        values[`${code}_modified`] = this.templateModifiedFields?.[code] || false;
                    }
                }
            } else {
                if (input.value.trim()) {
                    values[code] = input.value.trim();
                    values[`${code}_source`] = this.mapSource;
                    values[`${code}_modified`] = this.templateModifiedFields?.[code] || false;
                }
            }
        });
        return values;
    }

    // Function to create template form
    async createTemplateForm(schema) {
        try {
            const container = document.getElementById('templateContainer');
            if (!container) {
                console.error('Template container not found');
                return;
            }

            if (!schema || Object.keys(schema).length === 0) {
                console.error('Invalid or empty schema:', schema);
                return;
            }

            container.innerHTML = '';

            Object.entries(schema).forEach(([groupCode, group]) => {
                console.log('Processing group:', groupCode, group);
            
                if (!group.fields || !Array.isArray(group.fields)) {
                    console.error('Invalid fields format for group:', groupCode);
                    return;
                }

                const section = document.createElement('div');
                section.className = 'template-section mb-4';
                
                // Create header
                const header = document.createElement('div');
                header.className = 'template-section-header';
                header.setAttribute('data-bs-toggle', 'collapse');
                header.setAttribute('data-bs-target', `#section-${groupCode}`);
                header.setAttribute('aria-expanded', 'false');
                
                header.innerHTML = `
                    <div class="d-flex justify-content-between align-items-center">
                        <div class="template-section-title">
                            <span class="section-name">${group.name}</span>
                            <span class="section-code">${group.code}</span>
                        </div>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    ${group.description ? `<div class="template-section-description">${group.description}</div>` : ''}
                `;
                
                // Create collapsible content
                const content = document.createElement('div');
                content.className = 'collapse p-3';
                content.id = `section-${groupCode}`;

                const fieldsDiv = document.createElement('div');
                fieldsDiv.className = 'row g-1 mt-1';

                // Track if any fields in this section have values
                let hasValues = false;

                group.fields.forEach(field => {
                    const fieldDiv = this.createTemplateField(field);
                    fieldsDiv.appendChild(fieldDiv);

                    // Check if this field has a value in templateValues
                    if (this.templateValues?.values) {
                        const fieldValue = JSON.parse(this.templateValues.values)[field.code];
                        if (fieldValue) {
                            hasValues = true;
                        }
                    }
                });

                content.appendChild(fieldsDiv);
                section.appendChild(header);
                section.appendChild(content);
                container.appendChild(section);

                // If section has values, expand it
                if (hasValues) {
                    content.classList.add('show');
                    const icon = header.querySelector('.fas');
                    icon.classList.remove('fa-chevron-down');
                    icon.classList.add('fa-chevron-up');
                    header.setAttribute('aria-expanded', 'true');
                }
            });

            // Initialize Bootstrap collapse
            document.querySelectorAll('.template-section-header').forEach(header => {
                header.addEventListener('click', () => {
                    const content = header.nextElementSibling;
                    const icon = header.querySelector('.fas');
                    
                    // Add event listener to Bootstrap collapse event
                    content.addEventListener('show.bs.collapse', () => {
                        icon.classList.remove('fa-chevron-down');
                        icon.classList.add('fa-chevron-up');
                    });

                    content.addEventListener('hide.bs.collapse', () => {
                        icon.classList.remove('fa-chevron-up');
                        icon.classList.add('fa-chevron-down');
                    });
                });
            });
        } catch (error) {
            console.error('Error creating template form:', error);
            this.showError('Failed to create form template: ' + error.message);
        }
    }


    // Function to create template fields
    createTemplateField(field) {
        const div = document.createElement('div');
        div.className = 'col-md-6 mb-1 p-1 field-container';

        // Create label wrapper
        const labelWrapper = document.createElement('div');
        labelWrapper.className = 'd-flex align-items-center gap-2 mb-2';

        const label = document.createElement('label');
        label.className = 'form-label mb-0' + (field.required ? ' required-label' : '');
        label.textContent = field.name;

        // Add tooltip if help exists
        if (field.help || field.description) {
            const tooltipIcon = document.createElement('span');
            tooltipIcon.className = 'text-muted';
            tooltipIcon.innerHTML = `
                <i class="fas fa-info-circle" 
                data-bs-toggle="tooltip" 
                data-bs-placement="right"
                data-bs-html="true"
                title="${field.help || field.description}">
                </i>
            `;
            labelWrapper.appendChild(label);
            labelWrapper.appendChild(tooltipIcon);
        } else {
            labelWrapper.appendChild(label);
        }

        // Create and set up input
        let input;
        if (field.type === 'textarea') {
            input = document.createElement('textarea');
            input.className = 'form-control w-100';
            input.rows = field.options?.rows || 4;
        } else if (field.type === 'select') {
            input = document.createElement('select');
            input.className = 'form-select w-100';
            
            // Check if field has lookup mapping
            if (field.mapping?.lookup) {
                input.innerHTML = '<option value="">Loading...</option>';
                
                // Get the current value from templateValues if it exists
                if (this.templateValues?.values) {
                    const currentValues = JSON.parse(this.templateValues.values);
                    const idValue = currentValues[`${field.code}_id`];
                    if (idValue !== undefined) {
                        input.setAttribute('data-current-value', idValue);
                    }
                }
                
                this.populateLookupOptions(input, field.mapping.lookup.table, field.mapping.lookup.label, field.mapping.lookup.value);
            } else if (field.options?.values) {
                // Use default options if no lookup
                input.innerHTML = '<option value="">Select...</option>' +
                    field.options.values.map(opt => 
                        `<option value="${opt.value}">${opt.label}</option>`
                    ).join('');
            }

            // Add change event listener for fields that might have dependents
            input.addEventListener('change', (e) => {
                this.handleFieldChange(field.code, e.target.value);
            });
        } else if (field.type === 'time') {
            input = document.createElement('input');
            input.className = 'form-control w-100';
            input.type = 'time';
        } else {
            input = document.createElement('input');
            input.className = 'form-control w-100';
            input.type = field.type || 'text';
            input.placeholder = `Enter ${field.name.toLowerCase()}...`;
        }

        // Handle conditional fields
        if (field.conditional) {
            div.setAttribute('data-conditional-parent', field.conditional.field);
            div.setAttribute('data-conditional-value', field.conditional.value);
            div.style.display = 'none'; // Hide by default
            
            // Store the original required state on both div and input
            const isRequired = field.required;
            div.setAttribute('data-original-required', isRequired);
            input.setAttribute('data-original-required', isRequired);
            input.required = false; // Initially not required since hidden
            
            // Store original label state
            if (isRequired) {
                label.setAttribute('data-original-required', 'true');
            }
        } else {
            // For non-conditional fields, set required directly
            input.required = field.required;
        }

        // Add common attributes
        input.id = `template_${field.code}`;
        input.name = `template_${field.code}`;
        input.setAttribute('data-template-field', field.code);

        // Add validation rules
        if (field.options?.maxLength) {
            input.maxLength = field.options.maxLength;
        }

        div.appendChild(labelWrapper);
        div.appendChild(input);

        // Add event listener for mapped fields
        if (field.mapping?.source === this.mapSource) {
            input.addEventListener('change', () => this.handleTemplateFieldChange(input));
        }

        const validationContainer = document.createElement('div');
        validationContainer.className = 'validation-container';
        div.appendChild(validationContainer);

        return div;
    }

    // Function to handle template field change
    handleTemplateFieldChange(input) {
        const fieldCode = input.getAttribute('data-template-field');
        const field = this.findFieldByCode(fieldCode);
        
        if (field?.mapping?.source === this.mapSource) {
            // Mark field as modified
            this.templateModifiedFields = this.templateModifiedFields || {};
            this.templateModifiedFields[fieldCode] = true;
        }
    }

    // Function to find field by field code
    findFieldByCode(code) {
        if (!this.formTemplate?.template_schema) return null;
        const schema = JSON.parse(this.formTemplate.template_schema);
        
        for (const section of Object.values(schema)) {
            if (!section.fields) continue;
            
            const field = section.fields.find(f => f.code === code);
            if (field) return field;
        }
        
        return null;
    }

    // Function to setup the form
    setupForm() {
        // You can add processes here to setup the form (populate data, disabling the form, etc.)

        // Initialize tooltips
        this.initializeTooltips();
        
        this.bindEvents();
    }

    // Function to set the template Values
    setTemplateValues(values) {
        if (!values) {
            console.warn('No template values provided');
            return;
        }

        try {
            const parsed = typeof values === 'string' ? JSON.parse(values) : values;
            console.log('Parsed template values:', parsed);
            
            Object.entries(parsed).forEach(([code, value]) => {
                // Skip metadata fields
                if (code.endsWith('_source') || code.endsWith('_modified')) return;

                const input = document.querySelector(`[data-template-field="${code}"]`);
                if (!input) return;

                if (input.tagName.toLowerCase() === 'select') {
                    const field = this.findFieldByCode(code);
                    
                    // Handle lookup fields
                    if (field?.mapping?.lookup) {
                        // Use the corresponding ID value if it exists
                        const selectValue = parsed[code]; // This is the actual value to select
                        
                        // Find and select the correct option
                        Array.from(input.options).forEach(option => {
                            if (option.value === selectValue.toString()) {
                                option.selected = true;
                            }
                        });
                    } else {
                        // For non-lookup selects
                        input.value = value;
                    }
                } else {
                    // For non-select inputs
                    input.value = value;
                }
            });

            Object.entries(parsed).forEach(([code, value]) => {
                if (code.endsWith('_source') || code.endsWith('_modified')) return;
                
                // Check if the input has conditional values
                const input = document.querySelector(`[data-template-field="${code}"]`);
                if (input) {
                    this.handleFieldChange(code, input.value);
                }
            });

        } catch (error) {
            console.error('Error setting Template values:', error);
        }
    }

    // Function to check for conditional values
    handleFieldChange(fieldCode, value) {
        const dependentFields = document.querySelectorAll(`[data-conditional-parent="${fieldCode}"]`);
    
        dependentFields.forEach(field => {
            const requiredValue = field.getAttribute('data-conditional-value');
            const input = field.querySelector('[data-template-field]');
            const originalRequired = field.getAttribute('data-original-required') === 'true';
            const label = field.querySelector('.form-label');
            
            if (value === requiredValue) {
                field.style.display = 'block';
                if (input) {
                    input.required = originalRequired;
                    if (label && originalRequired) {
                        label.classList.add('required-label');
                    }
                }
            } else {
                field.style.display = 'none';
                if (input) {
                    input.required = false;
                    input.value = '';
                    if (label) {
                        label.classList.remove('required-label');
                    }
                    this.handleFieldChange(input.getAttribute('data-template-field'), '');
                }
            }
        });
    }

    // Function for form validation
    validateForm() {
        let isValid = true;
        this.clearValidationErrors();
        
        // Validate template fields
        if (!this.validateTemplateFields()) {
            isValid = false;
        }
        
        if (!isValid) {
            this.scrollToFirstError();
        }
        
        return isValid;
    }

    // Functionm to validate field from template
    validateTemplateFields() {
        let isValid = true;
        const requiredFields = document.querySelectorAll('[data-template-field][required]');
        
        requiredFields.forEach(input => {
            if (!this.validateField(input)) {
                isValid = false;
            }
        });
        
        return isValid;
    }

    // Function to highlight required fields
    highlightRequiredFields() {
        document.querySelectorAll('[data-template-field][required]').forEach(field => {
            if (!field.value.trim()) {
                this.addValidationError(field, 'This field is required');
                
                // Expand the section containing the field
                const section = field.closest('.collapse');
                if (section) {
                    const bsCollapse = bootstrap.Collapse.getInstance(section);
                    if (bsCollapse) {
                        bsCollapse.show();
                    }
                }
            }
        });
    }

    // Function to validate specific field
    validateField(input) {
        if (!input) return true;

        // Clear existing validation errors for this field
        this.clearValidationError(input);

        // Required validation
        if (input.required && !input.value.trim()) {
            this.addValidationError(input, 'This field is required');
            return false;
        }

        return true;
    }

    // Function to scroll to the first field error encountered
    scrollToFirstError() {
        const firstError = document.querySelector('.is-invalid');
        if (firstError) {
            // Expand section if it's collapsed
            const section = firstError.closest('.collapse');
            if (section) {
                const bsCollapse = bootstrap.Collapse.getInstance(section);
                if (bsCollapse) {
                    bsCollapse.show();
                }
            }

            // Smooth scroll to error
            setTimeout(() => {
                firstError.scrollIntoView({ 
                    behavior: 'smooth', 
                    block: 'center' 
                });
                
                // Highlight the field
                firstError.classList.add('highlight-error');
                setTimeout(() => {
                    firstError.classList.remove('highlight-error');
                }, 2000);
            }, 100); // Small delay to allow section expansion
        }
    }

    // Function to add validation error
    addValidationError(element, message) {
        const fieldContainer = element.closest('.field-container');
        if (!fieldContainer) return;

        // Remove any existing validation messages first
        const existingError = fieldContainer.querySelector('.validation-error');
        if (existingError) existingError.remove();

        element.classList.add('is-invalid');
        
        // Create and add new error message
        const errorDiv = document.createElement('div');
        errorDiv.className = 'validation-error';
        errorDiv.textContent = message;
        
        // Add the error message after the input element
        element.insertAdjacentElement('afterend', errorDiv);

        // Add error class to label
        const label = fieldContainer.querySelector('.form-label');
        if (label) {
            label.classList.add('text-danger');
        }
    }

    // Function to remove specific validation error
    clearValidationError(element) {
        const fieldContainer = element.closest('.field-container');
        if (!fieldContainer) return;

        fieldContainer.classList.remove('has-error');
        element.classList.remove('is-invalid');
        
        const errorDiv = fieldContainer.querySelector('.validation-error');
        if (errorDiv) {
            errorDiv.remove();
        }

        const label = fieldContainer.querySelector('.form-label');
        if (label) {
            label.classList.remove('text-danger');
        }
    }

    
    // Function to remove all validation errors
    clearValidationErrors() {
        // Remove all validation messages
        document.querySelectorAll('.validation-error').forEach(el => el.remove());
        
        // Remove validation classes
        document.querySelectorAll('.field-container').forEach(container => {
            container.classList.remove('has-error');
            const input = container.querySelector('[data-template-field]');
            if (input) input.classList.remove('is-invalid');
            const label = container.querySelector('.form-label');
            if (label) label.classList.remove('text-danger');
        });
    }

    /** Other Utility Functions **/

    // Function to get the variable set on the URL
    getRecordIdFromUrl() {
        const params = new URLSearchParams(window.location.search);
        return params.get('record_id'); // Change this to the variable you are using
    }

    // Function to initialize tooltips from template (help,description)
    initializeTooltips() {
        const tooltips = document.querySelectorAll('[data-bs-toggle="tooltip"]');
        tooltips.forEach(element => {
            const tooltip = bootstrap.Tooltip.getInstance(element);
            if (tooltip) {
                tooltip.dispose();
            }
            new bootstrap.Tooltip(element, {
                trigger: 'hover',
                placement: 'right',
                html: true,
                container: 'body'
            });
        });
    }

    // Sweet Alert Function on handling Errors
    showError(message) {
        Swal.fire({
            icon: 'error',
            title: 'Error',
            text: message
        });
    }
}

// Initialize form when document is ready
document.addEventListener('DOMContentLoaded', () => {
    window.recordsForm = new RecordsForm();
});
```

## 6. Template Examples

### 1. Basic Contact Form
```json
{
    "1.0": {
        "code": "1.0",
        "name": "Contact Information",
        "description": "Basic contact details",
        "fields": [
            {
                "code": "1.1",
                "name": "Full Name",
                "type": "text",
                "required": true,
                "options": {"maxLength": 100}
            },
            {
                "code": "1.2",
                "name": "Email",
                "type": "email",
                "required": true
            },
            {
                "code": "1.3",
                "name": "Message",
                "type": "textarea",
                "options": {"rows": 4}
            }
        ]
    }
}
```

### 2. Dynamic Form with Lookups
```json
{
    "1.0": {
        "code": "1.0",
        "name": "Employee Details",
        "fields": [
            {
                "code": "1.1",
                "name": "Department",
                "type": "select",
                "required": true,
                "mapping": {
                    "source": "departments",
                    "field": "dept_id",
                    "lookup": {
                        "table": "departments",
                        "label": "dept_name",
                        "value": "dept_id"
                    }
                }
            },
            {
                "code": "1.2",
                "name": "Position",
                "type": "select",
                "required": true,
                "conditional": {
                    "field": "1.1",
                    "operator": "exists"
                },
                "mapping": {
                    "source": "positions",
                    "field": "position_id",
                    "lookup": {
                        "table": "positions",
                        "label": "position_name",
                        "value": "position_id"
                    }
                }
            }
        ]
    }
}
```

# IMPORTANT NOTE
## Make sure to link your created routes on app/api.php and service on app/global.php
```php
    //On api.php
    include(dirname(__DIR__, 1) . "/app/api/Records.php");

    //On global.php
    include_once(dirname(__DIR__, 1) . "/app/lib/RecordsService.php");
```

This documentation provides a foundation for implementing a dynamic template generator. You can extend and modify it based on your specific needs.
