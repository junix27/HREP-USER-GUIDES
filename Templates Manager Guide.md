# Templates Manager User Guide

## Overview

The Templates Manager is a tool for building and managing JSON schema templates for the Archives Management System. This guide will help you understand how to create, edit, and manage metadata schemas that can be used throughout the system.

## Table of Contents

1. [Getting Started](#getting-started)
2. [Creating a New Template](#creating-a-new-template)
3. [Managing Sections](#managing-sections)
4. [Managing Fields](#managing-fields)
5. [Field Types](#field-types)
6. [Advanced Field Features](#advanced-field-features)
7. [Testing and Validating](#testing-and-validating)
8. [JSON Schema Reference](#json-schema-reference)

## Getting Started

To access the Schema Manager, navigate to the "Schema Manager" menu item in the main navigation. The interface consists of two main areas:

- **Left Sidebar**: Lists all available templates
- **Right Panel**: Schema editor for the selected template

## Creating a New Template

1. Click the "New Template" button at the top of the page
2. Enter a name for your template
3. Select whether the template should be active
4. Click "Save"

Once created, your template will appear in the list. Select it to begin adding sections and fields.

## Managing Sections

Sections are groups of related fields that help organize your metadata schema.

### Adding a Section

1. With a template selected, click the "Add Section" button
2. Enter a section code (e.g., "1.0") - this should be a unique identifier
3. Enter a section name
4. (Optional) Add a description for the section
5. Click "Save"

### Editing a Section

1. Click the "Edit" button on the section header
2. Update the section details
3. Click "Save"

### Deleting a Section

1. Click the "Delete" button on the section header
2. Confirm the deletion

**Note**: Deleting a section will also delete all fields within it.

## Managing Fields

Fields are the individual metadata elements that users will fill out.

### Adding a Field

1. Click the "Add Field" button on a section
2. Fill out the basic field information:
   - Field Code (e.g., "1.1")
   - Field Name
   - Field Type
   - Required (checkbox)
   - Help Text (tooltip text)
   - Description (longer explanation)
3. Configure field options appropriate to the chosen field type
4. Configure any mappings or conditional display
5. Click "Save Field"

### Editing a Field

1. Click the "Edit" button on a field
2. Update the field details
3. Click "Save Field"

### Deleting a Field

1. Click the "Delete" button on a field
2. Confirm the deletion

### Reordering Fields

You can drag and drop fields within a section to change their order.

## Field Types

The following field types are available:

### Text
A single-line text input field.
- **Options**:
  - Max Length: Maximum number of characters
  - Placeholder: Text shown when field is empty

### Textarea
A multi-line text input field.
- **Options**:
  - Rows: Number of visible rows
  - Max Length: Maximum number of characters
  - Placeholder: Text shown when field is empty

### Number
A numeric input field.
- **Options**:
  - Min: Minimum value
  - Max: Maximum value
  - Step: Increment value (default: 1)

### Date
A date picker field.
- **Options**:
  - Format: Date format (default: YYYY-MM-DD)

### Select
A dropdown selection field.
- **Options**:
  - Multiple: Allow multiple selections
  - Options: List of available options (value/label pairs)

### Radio
Radio buttons for selecting one option from a list.
- **Options**:
  - Inline: Display options horizontally
  - Options: List of available options (value/label pairs)

### Checkbox
Checkboxes for selecting multiple options from a list.
- **Options**:
  - Inline: Display options horizontally
  - Options: List of available options (value/label pairs)

## Advanced Field Features

### Database Mapping

Fields can be mapped to database fields to automatically populate or save data.

1. Go to the "Mapping" tab when editing a field
2. Check "Enable Database Mapping"
3. Configure:
   - Source Table: The database table (default: records)
   - Database Field: The field name in the database table
   - Use Lookup: For select fields, enable lookup from a reference table

### Lookup Configuration

For select fields that should get their options from a database table:

1. Enable "Database Mapping"
2. Check "Use Lookup Configuration"
3. Configure:
   - Lookup Table: Reference table name (e.g., "record_formats")
   - Value Field: Field to use as the option value (e.g., "record_format_id")
   - Label Field: Field to use as the option label (e.g., "record_format_name")

### Conditional Display

Fields can be configured to only appear when another field has a specific value:

1. Go to the "Conditional" tab when editing a field
2. Check "Enable Conditional Display"
3. Configure:
   - Controlling Field: Field that controls visibility
   - Required Value: Value the controlling field must have for this field to be visible

## Testing and Validating

After creating or modifying a template, use the Schema Validator & Preview tool to test it:

1. Navigate to "Schema Validator" in the main menu
2. Select your template from the dropdown
3. The JSON schema will appear in the left panel
4. A live preview of how the form will look will appear in the right panel
5. You can edit the JSON directly to experiment with changes
6. Click "Validate" to check for errors

## JSON Schema Reference

The schema format follows this structure:

```json
{
  "1.0": {
    "code": "1.0",
    "name": "Section Name",
    "description": "Section description",
    "fields": [
      {
        "code": "1.1",
        "name": "Field Name",
        "type": "text",
        "required": true,
        "options": {
          "maxLength": 100,
          "placeholder": "Enter text..."
        },
        "help": "Short help text",
        "description": "Longer description",
        "mapping": {
          "source": "records",
          "field": "database_field_name",
          "lookup": {
            "table": "lookup_table",
            "value": "id_field",
            "label": "name_field"
          }
        },
        "conditional": {
          "field": "1.2",
          "value": "specific_value"
        }
      }
    ]
  }
}
```

### Field Properties

| Property | Description |
|----------|-------------|
| code | Unique identifier for the field within the section |
| name | Display name for the field |
| type | Field type (text, textarea, select, etc.) |
| required | Whether the field is required (true/false) |
| options | Type-specific configuration options |
| help | Short help text displayed in a tooltip |
| description | Longer description text |
| mapping | Database mapping configuration |
| conditional | Conditional display configuration |
