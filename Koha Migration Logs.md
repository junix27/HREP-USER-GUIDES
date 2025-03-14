# KOHA MIGRATION LOGS

## Version 17.05 to 21.1200015

```
Upgrade to 17.12.00.016 done (Bug 18336 - Convert DB tables to utf8mb4 🎁)
Upgrade to 17.12.00.017 done (Bug 17672 - Add damaged_on to items and deleteditems tables)
Upgrade to 17.12.00.018 done (Bug 19290 - Add system preference BrowseResultSelection)
Upgrade to 17.12.00.019 done (Bug 20074 - Auth_subfield_structure changes hidden attribute)
Upgrade to 17.12.00.020 done (Bug 20082 - Update descriptions of Vietnamese language)
Upgrade to 17.12.00.021 done (Bug 13287 - Add system preference PurgeSuggestionsOlderThan)
Upgrade to 17.12.00.022 done (Bug 4078 - Add column currency.p_sep_by_space)
Upgrade to 17.12.00.023 done (Bug 20264 - Remove system preference 'checkdigit')
Upgrade to 17.12.00.024 done (Bug 15492 - Add a standalone self-checkin module)
Upgrade to 17.12.00.025 done (Bug 20291 - Add StaffLoginInstructions system preference and rename NoLoginInstructions with OpacLoginInstructions)
Upgrade to 17.12.00.026 done (Bug 19804 - Add issuingrules.suspension_chargeperiod)
Upgrade to 17.12.00.027 done (Bug 19289 - Add system preference UseACQFrameworkForBiblioRecords)
Upgrade to 17.12.00.028 done (Bug 9701 - Add default indicators (marc_tag_structure.indX_defaultvalue))
Upgrade to 17.12.00.029 done (Bug 14769 - Authorities merge: Set correct indicators in biblio field (new system preference AuthorityControlledIndicators))
Upgrade to 17.12.00.030 done (Bug 19882 - Add system preference NovelistSelectStaffProfile)
Upgrade to 17.12.00.031 done (Bug 11674 - Add system preference MarcFieldDocURL)
Upgrade to 17.12.00.032 done (Bug 19794 - Rename RLIST notice to SERIAL_ALERT)
Upgrade to 17.12.00.033 done (Bug 18786 - Add ability to create custom payment types)
Upgrade to 17.12.00.034 done (Bug 18790 - Add ability to void payment)
Upgrade to 17.12.00.035 done (Bug 19974 - Make MarkLostItemsAsReturned multiple)
Upgrade to 17.12.00.036 done (Bug 19287 - Add ability to mark an item 'Lost' from 'Holds to pull' list (CanMarkHoldsToPullAsLost, UpdateItemWhenLostFromHoldList and CANCEL_HOLD_ON_LOST))
Upgrade to 17.12.00.037 done (This change has been reverted, nothing done!)
Upgrade to 17.12.00.038 done (Bug 20245 - Use Bibliographic code value for Slovak language)
Upgrade to 17.12.00.039 done (Bug 20482 - Use Bibliographic code value for Basque, Maori and Albanian languages)
Upgrade to 17.12.00.040 done (Bug 20100 - Add new system preference ProtectSuperlibrarianPrivileges)
Upgrade to 17.12.00.041 done (Bug 11317 - Add a new permission to access files stored on the server)
Upgrade to 17.12.00.042 done (Bug 20402 - Implement OAuth2 authentication for REST API)
Upgrade to 17.12.00.043 done (Bug 20568 - Add API key management interface for patrons)
Upgrade to 17.12.00.044 done (Bug 20624 - Disable OAuth2 client credentials grant by default)
Upgrade to 18.05.00.000 done (Koha 18.05)
Upgrade to 18.06.00.000 done (Koha 18.06 - It's Adventure time!)
Upgrade to 18.06.00.001 done (Bug 3849- Improve descriptions of granular acquisition permissions)
Upgrade to 18.06.00.002 done (Bug 2426 - Remove deprecated management permission)
Upgrade to 18.06.00.003 done (Bug 20073 - Add new types for Elasticsearch fields)
Upgrade to 18.06.00.004 done (Bug 20980 - Manual credit offsets are stored as debits)
Upgrade to 18.06.00.005 done (Bug 12395 - Save order line's creator)
Upgrade to 18.06.00.006 done (Bug 19524 - Share patron lists between staff)
Upgrade to 18.06.00.007 done (Bug 7651 - Add separate permission for managing currencies and exchange rates)
Upgrade to 18.06.00.008 done (Bug 13560 - need an add option in marc modification templates)
Upgrade to 18.06.00.009 done (Bug 19166 - Add the ability to add adjustments to an invoice)
Upgrade to 18.06.00.010 done (Bug 19191 - Add ability to email receipts for account payments and write-offs)
Upgrade to 18.06.00.011 done (Bug 17698: Add column issues.noteseen and old_issues.noteseen)
Upgrade to 18.06.00.012 done (Bug 11911 - Add separate permission for managing suggestions)
Upgrade to 18.06.00.013 done (Bug 20997 - Add Koha::Account::Line::apply)
Upgrade to 18.06.00.014 done (Bug 21121 - New syspref to allow hiding of private patron data in circulation page)
Upgrade to 18.06.00.015 done (Bug 21226 - Remove prefs OCLCAffiliateID, XISBN and XISBNDailyLimit)
Upgrade to 18.06.00.016 done (Bug 20773 - expirationdate filled for waiting holds)
Upgrade to 18.06.00.017 done (Bug 21144: Add ROADTYPE to default authorised values categories)
Upgrade to 18.06.00.018 done (Bug 20487: Clear items.onloan for unissued items)
Upgrade to 18.06.00.019 done (Bug 19719: Default to hiding collection code column)
Upgrade to 18.06.00.020 done (Bug 15524 - Set limit on maximum possible holds per patron by category)
Upgrade to 18.06.00.021 done (Bug 21068 - Remove system preferences NorwegianPatronDB*)
Upgrade to 18.06.00.022 done (Bug 19383 - Add ability to print hold receipts automatically)
Upgrade to 18.06.00.023 done (Bug 18639 - Add replacementprice field to aqorders table)
Upgrade to 18.06.00.024 done (Bug 7534 - Let libraries have configuration for pickup locations)
Upgrade to 18.06.00.025 done (Bug 19817: Add pref KohaManualLanguage and KohaManualBaseURL)
Upgrade to 18.06.00.026 done (Bug 17530 - Add pref ArticleRequestsLinkControl)
Upgrade to 18.06.00.027 done (Bug 21235: Remove table services_throttle)
Upgrade to 18.06.00.028 done (Bug 19469 - Add ability to split view of holds view on record by pickup library and/or itemtype)
Upgrade to 18.06.00.029 done (Bug 21288: Slowness in acquisition caused by GetInvoices
Upgrade to 18.06.00.030 done (Bug 20777 - Remove unused field accountlines.dispute)
Upgrade to 18.06.00.031 done (Bug 20819: Add patron_consent)
Upgrade to 18.06.00.032 done (Bug 5458: length of items.ccode disagrees with authorised_values.authorised_value)
Upgrade to 18.06.00.033 done (Bug 12747 - Add AdditionalFieldsInZ3950ResultSearch system preference)
Upgrade to 18.06.00.034 done (Bug 17602 - Integrate support for OneClickdigital/Recorded Books API)
Upgrade to 18.06.00.035 done (Bug 21403 - Add Indian Amazon Affiliate option to AmazonLocale setting)
Upgrade to 18.06.00.036 done (Bug 18887 - Introduce new table 'circulation_rules', use for 'max_holds' rules)
Upgrade to 18.06.00.037 done (Bug 21082 - Add overdrive patron auth method)
Upgrade to 18.06.00.038 done (Bug 21417 - EDI ordering fails when basket and EAN libraries do not match)
Upgrade to 18.06.00.039 done (Bug 15520 - Add more granular permission for only editing own library's circ rules)
Upgrade to 18.06.00.040 done (Bug 11897 - Add Stock Rotation Feature)
Upgrade to 18.06.00.041 done (Bug 20772 - Add illrequestattributes.readonly and illrequest.price_paid columns)
Upgrade to 18.06.00.042 done (Bug 21617: Make statistics.ccode longer)
Upgrade to 18.06.00.043 done (Bug 15486: Restrict number of holds placed by day)
Upgrade to 18.06.00.044 done (Bug 15766: Add column creator_batches.description)
Upgrade to 18.06.00.045 done (Bug 21639 - Add phone transports by default)
Upgrade to 18.06.00.046 done (Bug 18591 - Add comments to ILL requests)
Upgrade to 18.06.00.047 done (Bug 19263 - Advanced Editor - Rancor - Add auto control number (001) widget)
Upgrade to 18.06.00.048 done (Bug 21682 - Remove default on stockrotationrotas.description)
Upgrade to 18.06.00.049 done (Bug 21656 - Stock Rotation Notice, Template Toolkit Syntax Correction)
Upgrade to 18.06.00.050 done (Bug 14385 - Add OpacHiddenItemExceptions)
Upgrade to 18.06.00.051 done (Bug 8630 - Add covers from AdLibris to the OPAC and Intranet)
Upgrade to 18.06.00.052 done (Bug 14391: Add granular permissions to the administration module)
Upgrade to 18.06.00.053 done (Bug 15494 - Block renewals by arbitrary item values)
Upgrade to 18.06.00.054 done (Bug 18316 - Add column search_field.weight)
Upgrade to 18.06.00.055 done (Bug 12365: Add column issuingrules.note)
Upgrade to 18.06.00.057 done (Bug 20312 - Add showLastPatron systempreference)
Upgrade to 18.06.00.058 done (Bug 19349 - Add system preferences MarcFieldForCreatorId, MarcFieldForCreatorName, MarcFieldForModifierId, MarcFieldForModifierName)
Upgrade to 18.06.00.059 done (Bug 20356 - Add EmailSMSSendDriverFromAddress system preference)
Upgrade to 18.06.00.060 done (Bug 15836 - Add class_sort_rules.split_routine and split_regex)
Upgrade to 18.06.00.061 done (Bug 19893 - Add elasticsearch index status preferences)
Upgrade to 18.06.00.062 done (Bug 21730: Add new authorised value category PA_CLASS)
Upgrade to 18.11.00.000 done (18.11.00 release)
Upgrade to 18.12.00.000 done (...and Steven!)
Upgrade to 18.12.00.001 (Bug 21961 - Fix typo in manage_didyoumean permission)
Upgrade to 18.12.00.002 done (Bug 21065 - Set ON DELETE SET NULL on accountlines.borrowernumber)
Upgrade to 18.12.00.003 done (Bug 22024 - Add missing splitting rule definitions)
Upgrade to 18.12.00.004 done (Bug 19066 - Add branchcode to accountlines)
Upgrade to 18.12.00.005 done (Bug 22030: Add OverDriveUsername syspref)
Upgrade to 18.12.00.006 done (Bug 21915 - Add a way to automatically reconcile balance for patrons)
Upgrade to 18.12.00.007 done (Bug 21753: Drop chargename from issuingrules )
Upgrade to 18.12.00.008 done (Bug 17047 - Mana knowledge base)
Upgrade to 18.12.00.009 done (Bug 21241 - Add FallbackToSMSIfNoEmail syspref )
Upgrade to 18.12.00.010 done (Bug 22061 - Add a /public namespace that can be switched on/off)
Upgrade to 18.12.00.011 done (Bug 22155 - biblio_metadata.marcflavour should be renamed 'schema')
Upgrade to 18.12.00.012 done (Bug 22132 - Add Basic authentication)
Upgrade to 18.12.00.013 done (Bug 22198 - Add ghranular permission setting for Mana KB)
Upgrade to 18.12.00.014 done (Bug 13515 - Add a FOREIGN KEY constaint on messages.borrowernumber)
Upgrade to 18.12.00.015 done (Bug 3820 - Update patron modification logs)
Upgrade to 18.12.00.016 done (Bug 20581 - Allow manual selection of custom ILL request statuses)
Upgrade to 18.12.00.017 done (Bug 21747 - Update account_offset_types to include 'fine_increase' and 'fine_decrease')
Upgrade to 18.12.00.018 done (Bug 19575 - Use canonical field names and resolve aliased fields)
Upgrade to 18.12.00.019 done (Bug 21728 - Add 'Reserve Fee' to the account_offset_types table if missing)
Upgrade to 18.12.00.020 done (Bug 18925 - Move maxissueqty and maxonsiteissueqty to circulation_rules)
Upgrade to 18.12.00.021 done (Bug 20912 - Support granular rental charges)
Upgrade to 18.12.00.022 done (Bug 15774 - Add permission for managing additional fields)
Upgrade to 18.12.00.023 done (Bug 20639 - Add ILLOpacbackends syspref)
Upgrade to 18.12.00.024 done (Bug 22368 - Add missing constraints to suggestions)
Upgrade to 18.12.00.025 done (Bug 21846 - Using emoji as tags has broken weights)
WARNING: (Bug 21846) You need to manually run /usr/share/koha/intranet/cgi-bin/misc/maintenance/fix_tags_weight.pl to fix possible issues with tags.
Upgrade to 18.12.00.026 done (Bug 20750 - Allow timestamped auditing of ILL request events)
Upgrade to 18.12.00.027 done (Bug 18837: Add ILLModuleUnmediated Syspref)
Upgrade to 18.12.00.028 done (Bug 21756 - Add 'Account Fee' and 'Hold Expired' to the account_offset_types table if missing)
Upgrade to 18.12.00.029 done (Bug 18736 - Add syspref to control order rounding)
Upgrade to 18.12.00.030 done (Bug 21683 - Remove accountlines.accountno and statistics.proccode fields)
Upgrade to 18.12.00.031 done (Bug 22008 - Add missing constraints for accountlines.manager_id)
Upgrade to 18.12.00.032 done (Bug 18235 - Elastic search - make facets configurable)
Upgrade to 18.12.00.033 done (Bug 18213 - Add language facets to Elasticsearch)
Upgrade to 18.12.00.034 done (Bug 22516 - Drop deprecated accountlines.lastincrement field)
Upgrade to 18.12.00.035 done (Bug 19722 - Add a MaxItemsToDisplayForBatchMod preference)
Upgrade to 18.12.00.036 done (Bug 22518 - Fix accounttype 'O' to 'FU' - 0 updated)
Upgrade to 18.12.00.037 done (Bug 22607 - Set default value of issues.renewals to 0)
Upgrade to 18.12.00.038 done (Bug 22512 - Add status to accountlines)
Upgrade to 18.12.00.039 done (Bug 22600 - Add interface to accountlines)
Upgrade to 18.12.00.040 done (Bug 12166 - Remove 'Reserve Charge' text from accountlines description)
Upgrade to 18.12.00.041 done (Bug 19670 - Change collation of marc_field to allow mixed case search field mappings)
Upgrade to 18.12.00.042 done (Bug 29891 - Remove non-XSLT detail view in the staff client)
Upgrade to 18.12.00.043 done (Bug 21953 - Remove 'Lost Item' text from accountlines description)
Upgrade to 18.12.00.044 done (Bug 21890 - Patron password reset by category)
Upgrade to 18.12.00.045 done (Bug 10796 - Patron password change by category)
Upgrade to 18.12.00.046 done (Bug 22695 - Remove non-XSLT search results view from the staff client)
Upgrade to 18.12.00.047 done (Bug 14557: Add Libris spellchecking system preferences)
Upgrade to 18.12.00.048 done (Bug 22044 - Set a default value for NoRenewalBeforePrecision)
Upgrade to 18.12.00.049 done (Bug 21336 - Add field flgAnonymized)
Upgrade to 18.12.00.050 done (Bug 21336 - Add preferences)
Upgrade to 18.12.00.051 done (Bug 21336 - Reset login_attempts)
Upgrade to 18.12.00.052 done (Bug 22311 - Add a SysPref to allow adding content to the #moresearches div in the opac)
Upgrade to 18.12.00.053 done (Bug 17171 - Add a syspref to allow currently issued items to be issued to a new patron without staff confirmation)
Upgrade to 18.12.00.054 done (Bug 20128: Add permission for Advanced Cataloging Editor)
Upgrade to 18.12.00.055 done (Bug 22521 - Update accountlines.accounttype to varchar(16), and map new statuses)
Upgrade to 18.12.00.056 done (Bug 8701 - Update OpacHiddenItems system preference description)
Upgrade to 18.12.00.057 done (Bug 13795 - Delete unused fields from statistics table)
Upgrade to 18.12.00.058 done (Bug 22318: Move contents of OpacNavRight preference to Koha news system)
Upgrade to 18.12.00.059 done (Bug 22532 - Remove import_records z3950random column)
Upgrade to 18.12.00.060 done (Bug 22564 - Fix accounttype 'Rep' - 0 updated)
Upgrade to 18.12.00.061 done (Bug 21336 - (follow-up) Rename flgAnonymized column)
Upgrade to 18.12.00.062 done (Bug 22339 - Fix search field mappings of MARC fixed fields)
Upgrade to 18.12.00.063 done (Bug 22511 - Update existing VOID accountlines)
Upgrade to 18.12.00.064 done (Bug 14576: Add UpdateItemLocationOnCheckin syspref)
Upgrade to 18.12.00.065 done (Bug 10300 - Allow transferring of items to be have separate IndependentBranches syspref)
Upgrade to 18.12.00.066 done (Bug 8995 - Add new preferences for OpenURLResolvers)
Upgrade to 18.12.00.067 done (Bug 8000 - Add new preferences for SendAllEmailsTo)
Upgrade to 18.12.00.068 done (Bug 7088: Cannot renew items on hold even with override)
Upgrade to 18.12.00.069 done (Bug 22053 - enable all plugins)
Upgrade to 18.12.00.070 done (Bug 14407 - Limit web-based self-checkout to specific IP addresses)
Upgrade to 18.12.00.071 done (Bug 22809 - Move 'ACCOUNT_CREDIT' from template to a slip)
Upgrade to 18.12.00.072 done (Bug 22809 - Move 'INVOICE' from template to a slip)
Upgrade to 18.12.00.073 done (Bug 5770 - Email librarian when purchase suggestion made)
Upgrade to 18.12.00.074 done (Bug 21411 - Add keyboard_shortcuts table)
Upgrade to 18.12.00.075 done (Bug 22899 - Add items constraint to tmp_holdsqueue)
Upgrade to 19.05.00.000 done (19.05.00 release)
Upgrade to 19.06.00.000 done (Wingardium Leviosa!)
Upgrade to 19.06.00.001 done (Bug 22960: Fix typo in syspref description)
Upgrade to 19.06.00.002 done (Bug 10215: Increase the size of opacnote and librariannote for table subscriptionhistory)
Upgrade to 19.06.00.003 done (Bug 22867: UniqueItemFields preference value should be pipe-delimited)
Upgrade to 19.06.00.004 done (Bug 22770: Fix typo in language description for el in German)
Upgrade to 19.06.00.005 done (Bug  9834: Add the reserves.item_level_hold column)
Upgrade to 19.06.00.006 done (Bug 21073: Improve plugin performance)
Upgrade to 19.06.00.007 done (Bug 22653: Remove unimplemented RotationPreventTransfers system preference)
Upgrade to 19.06.00.008 done (Bug 23109: Improve description of staffaccess permission)
Upgrade to 19.06.00.009 done (Bug 17178: add shortcut to keyboard_shortcuts)
Upgrade to 19.06.00.010 done (Bug 18928: Move holdallowed, hold_fulfillment_policy, returnbranch to circulation_rules)
Upgrade to 19.06.00.011 done (Bug 18930: Move lost item refund rules to circulation_rules table)
Upgrade to 19.06.00.012 done (Bug 22563: Fix accounttypes for 'L', 'LR' and 'CR')
Upgrade to 19.06.00.013 done (Bug 23151: Add borrower_modifications.changed_fields column)
Upgrade to 19.06.00.014 done (Bug 11573: Fix accounttypes for 'Rent')
Upgrade to 19.06.00.015 done (Bug 22524: Fix date/time-last-modified search with Elasticsearch)
Upgrade to 19.06.00.016 done (Bug 23396: Fix missing keyboard_shortcuts table)
Upgrade to 19.06.00.017 done (Bug 22610: Fix accounttypes for SIP2 payments)
Upgrade to 19.06.00.018 done (Bug 11529: Add medium, subtitle and part information to biblio table)
WARNING: Keyword to MARC Mappings:
    keyword: subtitle to field: 245$b for Default framework
    keyword: subtitle to field: 490$v for Default framework
    keyword: subtitle to field: 245$b for BKS framework
    keyword: subtitle to field: 245$b for SER framework
    keyword: subtitle to field: 245$b for LAWS framework
    keyword: subtitle to field: 245$c for LAWS framework
    keyword: title to field: 110$a for Default framework
    keyword: title to field: 110$a for BKS framework
    keyword: subtitle to field: 245$b for IRR framework
    keyword: subtitle to field: 245$b for ART framework
    keyword: subtitle to field: 773$t for ART framework
    keyword: subtitle to field: 773$g for ART framework
    keyword: date to field: 952$h for ART framework
    keyword: subtitle to field: 490$v for BKS framework
    keyword: subtitle to field: 245$c for Default framework
The keyword to marc mapping feature is no longer supported. Above find the
mappings that had been defined in your system. You will need to remap any
desired MARC fields to the Koha field you desire in the Koha to MARC mappings
page under Administration
NOTE: misc/batchRebuildBiblioTables.pl should be run to populate the fields introduced in bug 11529. It may take some time for larger databases.

Upgrade to 19.06.00.019 done (Bug 23228: Add option to automatically display payment receipt for printing after making a payment)
Upgrade to 19.06.00.020 done (Bug 23416: Add PreserveSerialNotes syspref)
Upgrade to 19.06.00.021 done (Bug 23309: Can't add new subfields to bibliographic frameworks in strict mode)
Upgrade to 19.06.00.022 done (Bug 14570: Make it possible to add multiple guarantors to a record)
Upgrade to 19.06.00.023 done (Bug 22258: Add ElasticsearchMARCFormat preference)
Upgrade to 19.06.00.024 done (Bug 23539: accountlines.accounttype should match authorised_values.authorised_value in size)
Upgrade to 19.06.00.025 done (Bug 22996: Add pref BarcodeSeparators)
Upgrade to 19.06.00.026 done (Bug 20691: Add ability for guarantors to view guarantee's fines in OPAC)
Upgrade to 19.06.00.027 done (Bug 15497: Add itemtypes_branches table)
Upgrade to 19.06.00.028 done (Bug 11573: Fix accounttypes for 'A')
Upgrade to 19.06.00.029 done (Bug 23321: Add cash_registers table, permissions and preferences)
Upgrade to 19.06.00.030 done (Bug 19618: add club_holds tables)
Upgrade to 19.06.00.031 done (Bug 23566: Add OPACDetailQRCode system preference)
Upgrade to 19.06.00.032 done (Bug 20589: Add field boosting and use elastic query fields parameter instead of depricated _all)
Upgrade to 19.06.00.033 done (Bug 23686: Add OnSiteCheckoutAutoCheck system preference)
Upgrade to 19.06.00.034 done (Bug 23007: Make transfer modals optionally block circ)
Upgrade to 19.06.00.035 done (Bug 18421: Add Coce image cache to the Intranet)
Upgrade to 19.06.00.036 done (Bug 20334: Add elasticsearch escape options preference)
Upgrade to 19.06.00.037 done (Bug 21701: PayPal return URL option)
Upgrade to 19.06.00.038 done (Bug 23697: Rename CircAutocompl system preference to PatronAutoComplete)
Upgrade to 19.06.00.039 done (Bug 17179: Add additional keyboard_shortcuts)
Upgrade to 19.06.00.040 done (Bug 17140: Add pref to allow rounding fines at payment)
Upgrade to 19.06.00.041 done (Bug 22880: Allow granular control of socialnetworks preference)
Upgrade to 19.06.00.042 done (Bug 22445: Add new pref *CustomCoverImages*)
Upgrade to 19.06.00.043 done (Bug 23049: Add account debit_types)
Upgrade to 19.06.00.044 done (Bug 23805: Add account credit_types)
Upgrade to 19.06.00.045 done (Bug 23866: Set HEA syspref to prompt for review)
Upgrade to 19.06.00.046 done (Bug 15260: Option for extended loan with useDaysMode)
Upgrade to 19.06.00.047 done (Bug 14697: Extend and enhance 'Claims returned' lost status)
Upgrade to 19.06.00.048 done (Bug 22581: add new OPACShowMusicalInscripts and OPACPlayMusicalInscripts system preferences)
Upgrade to 19.06.00.049 done (Bug 13958: Add a SuspensionsCalendar syspref)
Upgrade to 19.06.00.050 done (Bug 23293: Add 'OPACFineNoRenewalsIncludeCredits' system preference)
Upgrade to 19.11.00.000  [21:36:20]: 19.11.00 release
Upgrade to 19.12.00.000  [21:36:20]: Dobbie is a free elf...
Upgrade to 19.12.00.001  [21:36:20]: Bug 17831 - Remove non-existing bibliosubject.subject from frameworks
Upgrade to 19.12.00.002  [21:36:20]: Bug 23233 - Rename AllowItemsOnHoldCheckout syspref
Upgrade to 19.12.00.003  [21:36:20]: Bug 22284 - Add ft_local_hold_group column to library_groups
Upgrade to 19.12.00.004  [21:36:20]: Bug 24080 - Add PAYOUT account_debit_type
Upgrade to 19.12.00.005  [21:36:20]: Bug 24329 - Do not update action_log.timestamp
Upgrade to 19.12.00.006  [21:36:20]: Bug 24263 - Replace relationship with NULL when empty string
Upgrade to 19.12.00.007  [21:36:20]: Bug 23442 - Add REFUND to account_credit_types
Upgrade to 19.12.00.008  [21:36:20]: Bug 24206 - Update OpacSearchForTitleIn system preference
Upgrade to 19.12.00.009  [21:36:20]: Bug 23354 - Add 'Purchase' account offset type
Upgrade to 19.12.00.010  [21:36:20]: Bug 21520 - Add rule_order and rule_operator fields to oai_sets_mappings table
Upgrade to 19.12.00.011  [21:36:20]: Bug 24289 - Adding foreign keys on *_holidays.branchcode tables
Upgrade to 19.12.00.012  [21:36:20]: Bug 24481 - Move permission to correct module_bit
Upgrade to 19.12.00.013  [21:36:20]: Bug 24478 - Add `EnablePointOfSale` system preference to allow disabling the point of sale feature)
Upgrade to 19.12.00.014  [21:36:20]: Bug 24287 - Add 'reason' field to transfers table
Upgrade to 19.12.00.015  [21:36:20]: Bug 24296 - Update stockrotation to use 'reason' field in transfers table
Upgrade to 19.12.00.016  [21:36:20]: Bug 22868 - Move suggestions_manage subpermission out of acquisition permission
Upgrade to 19.12.00.017  [21:36:20]: Bug 21674 - Add unique key (parent_id, branchcode) to library_group
Upgrade to 19.12.00.018  [21:36:20]: Bug 18936 - Convert issuingrules fields to circulation_rules
Upgrade to 19.12.00.019  [21:36:21]: Bug 23673 - modify time_queued and add updated_on to message_queue
Upgrade to 19.12.00.020  [21:36:21]: Bug  8643 - Add important constraint to marc subfields
Upgrade to 19.12.00.021  [21:36:21]: Bug 24592 - Update LOST_RETURN to LOST_FOUND
Upgrade to 19.12.00.022  [21:36:22]: Bug 20882 - items.uri to MEDIUMTEXT
Upgrade to 19.12.00.023  [21:36:22]: Bug 24640 - Allow quotes.timestamp to be NULL
Upgrade to 19.12.00.024  [21:36:22]: Bug 21633 - Remove finesMode "test"
Upgrade to 19.12.00.025  [21:36:22]: Bug 24103 - add DumpSearchQueryTemplate syspref
Upgrade to 19.12.00.026  [21:36:22]: Bug 11297 - Add support for custom PQF attributes for Z39.50 server searches
Upgrade to 19.12.00.027  [21:36:22]: Bug 24532 - Fix pathological cases of negative debits
Upgrade to 19.12.00.028  [21:36:22]: Bug 14567 - Add OpacBrowseSearch syspref
Upgrade to 19.12.00.029  [21:36:22]: Bug 17702 - Add column account_credit_types.archived
Upgrade to 19.12.00.030  [21:36:22]: Bug 22880 - Move contents of opacheader preference to Koha news system
Upgrade to 19.12.00.031  [21:36:22]: Bug 22273 - Column article_requests.created_on should not be updated
Upgrade to 19.12.00.032  [21:36:22]: Bug 24735 - Remove UseQueryParser system preference
Upgrade to 19.12.00.033  [21:36:22]: Bug 23355 - Add cash_register_actions table
Upgrade to 19.12.00.034  [21:36:22]: Bug 24081 - Add DISCOUNT to account_credit_types and account_offset_types, Add accounts discount permission
Upgrade to 19.12.00.035  [21:36:22]: Bug 23442 - Add a refund option to the point of sale system
Upgrade to 19.12.00.036  [21:36:22]: Bug 24369 - Add CORS support to Koha
Upgrade to 19.12.00.037  [21:36:22]: Bug 23051 - Add RenewAccruingItemInOpac syspref
Upgrade to 19.12.00.038  [21:36:22]: Bug 23112 - Add CirculateILL syspref
Upgrade to 19.12.00.039  [21:36:22]: Bug 17845 - Drop unused table printers and branchprinter column
Upgrade to 19.12.00.040  [21:36:22]: Bug 17374 - Update description of DefaultPatronSearchFields
Upgrade to 19.12.00.041  [21:36:22]: Bug 24722 - Enforce NOT NULL constraint for reserves.priority
Upgrade to 19.12.00.042  [21:36:22]: Bug 22821 - Add reply_address to message_queue
Upgrade to 19.12.00.043  [21:36:22]: Bug 24296 - Add 'return' reasons to branchtransfers enum
Upgrade to 19.12.00.044  [21:36:22]: Bug 24846 - Add a new permission for new tool batch extend due dates
Upgrade to 19.12.00.045  [21:36:22]: Bug  4461 - Add CollapseFieldsPatronAddForm system preference
Upgrade to 19.12.00.046  [21:36:22]: Bug 24818 - Update 'accountlines.date' from DATE to TIMESTAMP
Upgrade to 19.12.00.047  [21:36:22]: Bug 22987 - Add biblioimages.timestamp
Upgrade to 19.12.00.048  [21:36:22]: Bug 24299 - Add 'collection' reasons to branchtransfers enum
Upgrade to 19.12.00.049  [21:36:22]: Bug 24299 - Add 'reserve' reasons to branchtransfers enum
Upgrade to 19.12.00.050  [21:36:22]: Bug 24854 - Remove IDreamBooks* system preferences
Upgrade to 19.12.00.051  [21:36:22]: Bug 24759 - Cleanup OpacRenewalBranch
Upgrade to 19.12.00.052  [21:36:22]: Bug 21443 - Add ability to exclude holidays when calculating rentals fees by time period
Upgrade to 19.12.00.053  [21:36:22]: Bug 24476 - Allow patrons to opt-out of autorenewal
Upgrade to 19.12.00.054  [21:36:22]: Bug 13881 - Add desk management
Upgrade to 19.12.00.055  [21:36:22]: Bug 23590 - Add lastmodificationby and lastmodificationdate to the suggestions table
Upgrade to 19.12.00.056  [21:36:22]: Bug 20415 - Remove UseKohaPlugins preference
Upgrade to 19.12.00.057  [21:36:22]: Bug 20399 - Remove INTRAdidyoumean preference
Upgrade to 19.12.00.058  [21:36:22]: Bug 14715 - Add sysprefs numSearchResultsDropdown and OPACnumSearchResultsDropdown
Upgrade to 19.12.00.059  [21:36:22]: Bug 18177 - Remove some unused columns from aqbooksellers
Upgrade to 19.12.00.060  [21:36:22]: Bug 23204 - Change enum order for marc_type in search_marc_map to fix sorting
Upgrade to 19.12.00.061  [21:36:22]: Bug 24474 - Add `onpayment` option to MarkLostItemsAsReturned
Upgrade to 19.12.00.062  [21:36:22]: Bug 25010 - Fix typo in account_debit_type description
Upgrade to 19.12.00.063  [21:36:22]: Bug 22534 - Add PreFillGuaranteeField syspref
Upgrade to 19.12.00.064  [21:36:22]: Bug  4944 - Add new system preference OpacNoItemTypeImages
Upgrade to 19.12.00.065  [21:36:22]: Bug 23173 - Add ILLCheckAvailability syspref
Upgrade to 19.12.00.066  [21:36:22]: Bug  4461 - Add OPACReportProblem system preference
Upgrade to 19.12.00.067  [21:36:22]: Bug 20754 - Remove double accepted list shares
Upgrade to 19.12.00.068  [21:36:22]: Bug 21190 - Add prefs AuthFailureLog and AuthSuccessLog
Upgrade to 19.12.00.069  [21:36:22]: Bug 22784 - Add a new suggestions.archived column
Upgrade to 19.12.00.070  [21:36:22]: Bug 22774 - Limit purchase suggestion in a specified time period
Add unique constraint to authorised_values at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 21650.
WARNING - Cannot create unique constraint on authorised_value(category, authorised_value) at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 21650.
The following entries are duplicated: HSBND_FREQ:EW (2), REPORT_GROUP:SER (2) at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 21650.
Upgrade to 19.12.00.071  [21:36:22]: Bug 22887 - Add unique constraint to authorised_values
Upgrade to 19.12.00.072  [21:36:22]: Bug 24380 - Add syspref CalculateFinesOnBackdate
Upgrade to 19.12.00.073  [21:36:22]: Bug 25152 - Update subscription.closed to tinyint(1) as per guidelines
Upgrade to 19.12.00.074  [21:36:22]: Bug 25147 - Rename AllowSelfCheckReturns to SCOAllowCheckin for consistency
Upgrade to 19.12.00.075  [21:36:23]: Bug 25086 - Set changed_fields column of borrower_modifications as nullable
WARNING - The following serials are deleted, they were not attached to an existing bibliographic record (serialid): 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219, 220, 221, 222, 223, 224, 225, 226, 227, 228, 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260, 261, 262, 263, 264, 265, 266, 267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 351, 352, 353, 354, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370, 371, 372, 373, 374, 375, 376, 377, 378, 379, 380, 381, 382, 383, 384, 385, 386, 387, 388, 389, 390, 391, 392, 393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 483, 484, 485, 486, 487, 488, 489, 490, 491, 492, 493, 494, 495, 496, 497, 498, 499, 500, 501, 502, 503, 504, 505, 506, 507, 508, 509, 510, 511, 512, 513, 514, 515, 516, 517, 518, 519, 520, 521, 522, 523, 524, 525, 526, 527, 528, 529, 530, 531, 532, 533, 534, 535, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 546, 547, 548, 549, 550, 551, 552, 553, 554, 555, 556, 557, 558, 559, 560, 561, 562, 563, 564, 565, 566, 567, 568, 569, 570, 571, 572, 573, 574, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586, 587, 588, 589, 590, 591, 592, 593, 594, 595, 596, 597, 598, 599, 600, 601, 602, 603, 604, 605, 606, 607, 608, 609, 610, 611, 612, 613, 614, 615, 616, 617, 618, 619, 620, 621, 622, 623, 624, 625, 626, 627, 628, 629, 630, 631, 632, 633, 634, 635, 636, 637, 638, 639, 640, 641, 642, 643, 644, 645, 646, 647, 648, 649, 650, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 673, 674, 675, 676, 677, 678, 679, 680, 681, 682, 683, 684, 685, 686, 687, 688, 689, 690, 691, 692, 693, 694, 695, 696, 697, 698, 699, 700, 701, 702, 703, 704, 705, 706, 707, 708, 709, 710, 711, 712, 713, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763, 764, 765, 766, 767, 768, 769, 770, 771, 772, 773, 774, 775, 776, 777, 778, 779, 780, 781, 782, 783, 784, 785, 786, 787, 788, 789, 790, 791, 792, 793, 794, 795, 796, 797, 798, 799, 800, 801, 802, 803, 804, 805, 806, 807, 808, 809, 810, 811, 812, 813, 814, 815, 816, 817, 818, 819, 820, 821, 822, 823, 824, 825, 826, 827, 828, 829, 830, 831, 832, 833, 834, 835, 836, 837, 838, 839, 840, 841, 842, 843, 844, 845, 846, 847, 848, 849, 850, 851, 852, 853, 854, 855, 856, 857, 858, 859, 860, 861, 862, 863, 864, 865, 866, 867, 868, 869, 870, 871, 872, 873, 874, 875, 876, 877, 878, 879, 880, 881, 882, 883, 884, 885, 886, 887, 888, 889, 890, 891, 892, 893, 894, 895, 896, 897, 898, 899, 900, 901, 902, 903, 904, 905, 906, 907, 908, 909, 910, 911, 912, 913, 914, 915, 916, 917, 918, 919, 920, 921, 922, 923, 924, 925, 926, 927, 928, 929, 930, 931, 932, 933, 934, 935, 936, 937, 938, 939, 940, 941, 942, 943, 944, 945, 946, 947, 948, 949, 950, 951, 952, 953, 954, 955, 956, 957, 958, 959, 960, 961, 962, 963, 964, 965, 966, 967, 968, 969, 970, 971, 972, 973, 974, 975, 976, 977, 978, 979, 980, 981, 982, 983, 984, 985, 986, 987, 988, 989, 990, 991, 992, 993, 994, 995, 996, 997, 998, 999, 1000, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1008, 1009, 1010, 1011, 1012, 1013, 1014, 1015, 1016, 1017, 1018, 1019, 1020, 1021, 1022, 1023, 1024, 1025, 1026, 1027, 1028, 1029, 1030, 1031, 1032, 1033, 1034, 1035, 1036, 1037, 1038, 1039, 1040, 1041, 1042, 1043, 1044, 1045, 1046, 1047, 1048, 1049, 1050, 1051, 1052, 1053, 1054, 1055, 1056, 1057, 1058, 1059, 1060, 1061, 1062, 1063, 1064, 1065, 1066, 1067, 1068, 1069, 1070, 1071, 1072, 1073, 1074, 1075, 1076, 1077, 1078, 1079, 1080, 1081, 1082, 1083, 1084, 1085, 1086, 1087, 1088, 1089, 1090, 1091, 1092, 1093, 1094, 1095, 1096, 1097, 1098, 1099, 1100, 1101, 1102, 1103, 1104, 1105, 1106, 1107, 1108, 1109, 1110, 1111, 1112, 1113, 1114, 1115, 1116, 1117, 1118, 1119, 1120, 1121, 1122, 1123, 1124, 1125, 1126, 1127, 1128, 1129, 1130, 1131, 1132, 1133, 1134, 1135, 1136, 1137, 1138, 1139, 1140, 1141, 1142, 1143, 1144, 1145, 1146, 1147, 1148, 1149, 1150, 1151, 1152, 1153, 1154, 1155, 1156, 1157, 1158, 1159, 1160, 1161, 1162, 1163, 1164, 1165, 1166, 1167, 1168, 1169, 1170, 1171, 1172, 1173, 1174, 1175, 1176, 1177, 1178, 1179, 1180, 1181, 1182, 1183, 1184, 1185, 1186, 1187, 1188, 1189, 1190, 1191, 1192, 1193, 1194, 1195, 1196, 1197, 1198, 1199, 1200, 1201, 1202, 1203, 1204, 1205, 1206, 1207, 1208, 1209, 1210, 1211, 1212, 1213, 1214, 1215, 1216, 1217, 1218, 1219, 1220, 1221, 1222, 1223, 1224, 1225, 1226, 1227, 1228, 1229, 1230, 1231, 1232, 1233, 1234, 1235, 1236, 1237, 1238, 1239, 1240, 1241, 1242, 1243, 1244, 1245, 1246, 1247, 1248, 1249, 1250, 1251, 1252, 1253, 1254, 1255, 1256, 1257, 1258, 1259, 1260, 1261, 1262, 1263, 1264, 1265, 1266, 1267, 1268, 1269, 1270, 1271, 1272, 1273, 1274, 1275, 1276, 1277, 1278, 1279, 1280, 1281, 1282, 1283, 1284, 1285, 1286, 1287, 1288, 1289, 1290, 1291, 1292, 1293, 1294, 1295, 1296, 1297, 1298, 1299, 1300, 1301, 1302, 1303, 1304, 1305, 1306, 1307, 1308, 1309, 1310, 1311, 1312, 1313, 1314, 1315, 1316, 1317, 1318, 1319, 1320, 1321, 1322, 1323, 1324, 1325, 1326, 1327, 1328, 1329, 1330, 1331, 1332, 1333, 1334, 1335, 1336, 1337, 1338, 1339, 1340, 1341, 1342, 1343, 1344, 1345, 1346, 1347, 1348, 1349, 1350, 1351, 1352, 1353, 1354, 1355, 1356, 1357, 1358, 1359, 1360, 1361, 1362, 1363, 1364, 1365, 1366, 1367, 1368, 1369, 1370, 1371, 1372, 1373, 1374, 1375, 1376, 1377, 1378, 1379, 1380, 1381, 1382, 1383, 1384, 1385, 1386, 1387, 1388, 1389, 1390, 1391, 1392, 1393, 1394, 1395, 1396, 1397, 1398, 1399, 1400, 1401, 1402, 1403, 1404, 1405, 1406, 1407, 1408, 1409, 1410, 1411, 1412, 1413, 1414, 1415, 1416, 1417, 1418, 1419, 1420, 1421, 1422, 1423, 1424, 1425, 1426, 1427, 1428, 1429, 1430, 1431, 1432, 1433, 1434, 1435, 1436, 1437, 1438, 1439, 1440, 1441, 1442, 1443, 1444, 1445, 1446, 1447, 1448, 1449, 1450, 1451, 1452, 1453, 1454, 1455, 1456, 1457, 1458, 1459, 1460, 1461, 1462, 1463, 1464, 1465, 1466, 1467, 1468, 1469, 1470, 1471, 1472, 1473, 1474, 1475, 1476, 1477, 1478, 1479, 1480, 1481, 1482, 1483, 1484, 1485, 1486, 1487, 1488, 1489, 1490, 1491, 1492, 1493, 1494, 1495, 1496, 1497, 1498, 1499, 1500, 1501, 1502, 1503, 1504, 1505, 1506, 1507, 1508, 1509, 1510, 1511, 1512, 1513, 1514, 1515, 1516, 1517, 1518, 1519, 1520, 1521, 1522, 1523, 1524, 1525, 1526, 1527, 1528, 1529, 1530, 1531, 1532, 1533, 1534, 1535, 1536, 1537, 1538, 1539, 1540, 1541, 1542, 1543, 1544, 1545, 1546, 1547, 1548, 1549, 1550, 1551, 1552, 1553, 1554, 1555, 1556, 1557, 1558, 1559, 1560, 1561, 1562, 1563, 1564, 1565, 1566, 1567, 1568, 1569, 1570, 1571, 1572, 1573, 1574, 1575, 1576, 1577, 1578, 1579, 1580, 1581, 1582, 1583, 1584, 1585, 1586, 1587, 1588, 1589, 1590, 1591, 1592, 1593, 1594, 1595, 1596, 1597, 1598, 1599, 1600, 1601, 1602, 1603, 1604, 1605, 1606, 1607, 1608, 1609, 1610, 1611, 1612, 1613, 1614, 1615, 1616, 1617, 1618, 1619, 1620, 1621, 1622, 1623, 1624, 1625, 1626, 1627, 1628, 1629, 1630, 1631, 1632, 1633, 1634, 1635, 1636, 1637, 1638, 1639, 1640, 1641, 1642, 1643, 1644, 1645, 1646, 1647, 1648, 1649, 1650, 1651, 1652, 1653, 1654, 1655, 1656, 1657, 1658, 1659, 1660, 1661, 1662, 1663, 1664, 1665, 1666, 1667, 1668, 1669, 1670, 1671, 1672, 1673, 1674, 1675, 1676, 1677, 1678, 1679, 1680, 1681, 1682, 1683, 1684, 1685, 1686, 1687, 1688, 1689, 1690, 1691, 1692, 1693, 1694, 1695, 1696, 1697, 1698, 1699, 1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707, 1708, 1709, 1710, 1711, 1712, 1713, 1714, 1715, 1716, 1717, 1718, 1719, 1720, 1721, 1722, 1723, 1724, 1725, 1726, 1727, 1728, 1729, 1730, 1731, 1732, 1733, 1734, 1735, 1736, 1737, 1738, 1739, 1740, 1741, 1742, 1743, 1744, 1745, 1746, 1747, 1748, 1749, 1750, 1751, 1752, 1753, 1754, 1755, 1756, 1757, 1758, 1759, 1760, 1761, 1762, 1763, 1764, 1765, 1766, 1767, 1768, 1769, 1770, 1771, 1772, 1773, 1774, 1775, 1776, 1777, 1778, 1779, 1780, 1781, 1782, 1783, 1784, 1785, 1786, 1787, 1788, 1789, 1790, 1791, 1792, 1793, 1794, 1795, 1796, 1797, 1798, 1799, 1800, 1801, 1802, 1803, 1804, 1805, 1806, 1807, 1808, 1809, 1810, 1811, 1812, 1813, 1814, 1815, 1816, 1817, 1818, 1819, 1820, 1821, 1822, 1823, 1824, 1825, 1826, 1827, 1828, 1829, 1830, 1831, 1832, 1833, 1834, 1835, 1836, 1837, 1838, 1839, 1840, 1841, 1842, 1843, 1844, 1845, 1846, 1847, 1848, 1849, 1850, 1851, 1852, 1853, 1854, 1855, 1856, 1857, 1858, 1859, 1860, 1861, 1862, 1863, 1864, 1865, 1866, 1867, 1868, 1869, 1870, 1871, 1872, 1873, 1874, 1875, 1876, 1877, 1878, 1879, 1880, 1881, 1882, 1883, 1884, 1885, 1886, 1887, 1888, 1889, 1890, 1891, 1892, 1893, 1894, 1895, 1896, 1897, 1898, 1899, 1900, 1901, 1902, 1903, 1904, 1905, 1906, 1907, 1908, 1909, 1910, 1911, 1912, 1913, 1914, 1915, 1916, 1917, 1918, 1919, 1920, 1921, 1922, 1923, 1924, 1925, 1926, 1927, 1928, 1929, 1930, 1931, 1932, 1933, 1934, 1935, 1936, 1937, 1938, 1939, 1940, 1941, 1942, 1943, 1944, 1945, 1946, 1947, 1948, 1949, 1950, 1951, 1952, 1953, 1954, 1955, 1956, 1957, 1958, 1959, 1960, 1961, 1962, 1963, 1964, 1965, 1966, 1967, 1968, 1969, 1970, 1971, 1972, 1973, 1974, 1975, 1976, 1977, 1978, 1979, 1980, 1981, 1982, 1983, 1984, 1985, 1986, 1987, 1988, 1989, 1990, 1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998, 1999, 2000, 2001, 2002, 2003, 2004, 2005, 2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023, 2024, 2025, 2026, 2027, 2028, 2029, 2030, 2031, 2032, 2033, 2034, 2035, 2036, 2037, 2038, 2039, 2040, 2041, 2042, 2043, 2044, 2045, 2046, 2047, 2048, 2049, 2050, 2051, 2052, 2053, 2054, 2055, 2056, 2057, 2058, 2059, 2060, 2061, 2062, 2063, 2064, 2065, 2066, 2067, 2068, 2069, 2070, 2071, 2072, 2073, 2074, 2075, 2076, 2077, 2078, 2079, 2080, 2081, 2082, 2083, 2084, 2085, 2086, 2087, 2088, 2089, 2090, 2091, 2092, 2093, 2094, 2095, 2096, 2097, 2098, 2099, 2100, 2101, 2102, 2103, 2104, 2105, 2106, 2107, 2108, 2109, 2110, 2111, 2112, 2113, 2114, 2115, 2116, 2117, 2118, 2119, 2120, 2121, 2122, 2123, 2124, 2125, 2126, 2127, 2128, 2129, 2130, 2131, 2132, 2133, 2134, 2135, 2136, 2137, 2138, 2139, 2140, 2141, 2142, 2143, 2144, 2145, 2146, 2147, 2148, 2149, 2150, 2151, 2152, 2153, 2154, 2155, 2156, 2157, 2158, 2159, 2160, 2161, 2162, 2163, 2164, 2165, 2166, 2167, 2168, 2169, 2170, 2171, 2172, 2173, 2174, 2175, 2176, 2177, 2178, 2179, 2180, 2181, 2182, 2183, 2184, 2185, 2186, 2187, 2188, 2189, 2190, 2191, 2192, 2193, 2194, 2195, 2196, 2197, 2198, 2199, 2200, 2201, 2202, 2203, 2204, 2205, 2206, 2207, 2208, 2209, 2210, 2211, 2212, 2213, 2214, 2215, 2216, 2217, 2218, 2219, 2220, 2221, 2222, 2223, 2224, 2225, 2226, 2227, 2228, 2229, 2230, 2231, 2232, 2233, 2234, 2235, 2236, 2237, 2238, 2239, 2240, 2241, 2242, 2243, 2244, 2245, 2246, 2247, 2248, 2249, 2250, 2251, 2252, 2253, 2254, 2255, 2256, 2257, 2258, 2259, 2260, 2261, 2262, 2263, 2264, 2265, 2266, 2267, 2268, 2269, 2270, 2271, 2272, 2273, 2274, 2275, 2276, 2277, 2278, 2279, 2280, 2281, 2282, 2283, 2284, 2285, 2286, 2287, 2288, 2289, 2290, 2291, 2292, 2293, 2294, 2295, 2296, 2297, 2298, 2299, 2300, 2301, 2302, 2303, 2304, 2305, 2306, 2307, 2308, 2309, 2310, 2311, 2312, 2313, 2314, 2315, 2316, 2317, 2318, 2319, 2320, 2321, 2322, 2323, 2324, 2325, 2326, 2327, 2328, 2329, 2330, 2331, 2332, 2333, 2334, 2335, 2336, 2337, 2338, 2339, 2340, 2341, 2342, 2343, 2344, 2345, 2346, 2347, 2348, 2349, 2350, 2351, 2352, 2353, 2354, 2355, 2356, 2357, 2358, 2359, 2360, 2361, 2362, 2363, 2364, 2365, 2366, 2367, 2368, 2369, 2370, 2371, 2372, 2373, 2374, 2375, 2376, 2377, 2378, 2379, 2380, 2381, 2382, 2383, 2384, 2385, 2386, 2387, 2388, 2389, 2390, 2391, 2392, 2393, 2394, 2395, 2396, 2397, 2398, 2399, 2400, 2401, 2402, 2403, 2404, 2405, 2406, 2407, 2408, 2409, 2410, 2411, 2412, 2413, 2414, 2415, 2416, 2417, 2418, 2419, 2420, 2421, 2422, 2423, 2424, 2425, 2426, 2427, 2428, 2429, 2430, 2431, 2432, 2433, 2434, 2435, 2436, 2437, 2438, 2439, 2440, 2441, 2442, 2443, 2444, 2445, 2446, 2447, 2448, 2449, 2450, 2451, 2452, 2453, 2454, 2455, 2456, 2457, 2458, 2459, 2460, 2461, 2462, 2463, 2464, 2465, 2466, 2467, 2468, 2469, 2470, 2471, 2472, 2473, 2474, 2475, 2476, 2477, 2478, 2479, 2480, 2481, 2482, 2483, 2484, 2485, 2486, 2487, 2488, 2489, 2490, 2491, 2492, 2493, 2494, 2495, 2496, 2497, 2498, 2499, 2500, 2501, 2502, 2503, 2504, 2505, 2506, 2507, 2508, 2509, 2510, 2511, 2512, 2513, 2514, 2515, 2516, 2517, 2518, 2519, 2520, 2521, 2522, 2523, 2524, 2525, 2526, 2527, 2528, 2529, 2530, 2531, 2532, 2533, 2534, 2535, 2536, 2537, 2538, 2539, 2540, 2541, 2542, 2543, 2544, 2545, 2546, 2547, 2548, 2549, 2550, 2551, 2552, 2553, 2554, 2555, 2556, 2557, 2558, 2559, 2560, 2561, 2562, 2563, 2564, 2565, 2566, 2567, 2568, 2569, 2570, 2571, 2572, 2573, 2574, 2575, 2576, 2577, 2578, 2579, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2589, 2590, 2591, 2592, 2593, 2594, 2595, 2596, 2597, 2598, 2599, 2600, 2601, 2602, 2603, 2604, 2605, 2606, 2607, 2608, 2609, 2610, 2611, 2612, 2613, 2614, 2615, 2616, 2617, 2618, 2619, 2620, 2621, 2622, 2623, 2624, 2625, 2626, 2627, 2628, 2629, 2630, 2631, 2632, 2633, 2634, 2635, 2636, 2637, 2638, 2639, 2640, 2641, 2642, 2643, 2644, 2645, 2646, 2647, 2648, 2649, 2650, 2651, 2652, 2653, 2654, 2655, 2656, 2657, 2658, 2659, 2660, 2661, 2662, 2663, 2664, 2665, 2666, 2667, 2668, 2669, 2670, 2671, 2672, 2673, 2674, 2675, 2676, 2677, 2678, 2679, 2680, 2681, 2682, 2683, 2684, 2685, 2686, 2687, 2688, 2689, 2690, 2691, 2692, 2693, 2694, 2695, 2696, 2697, 2698, 2699, 2700, 2701, 2702, 2703, 2704, 2705, 2706, 2707, 2708, 2709, 2710, 2711, 2712, 2713, 2714, 2715, 2716, 2717, 2718, 2719, 2720, 2721, 2722, 2723, 2724, 2725, 2726, 2727, 2728, 2729, 2730, 2731, 2732, 2733, 2734, 2735, 2736, 2737, 2738, 2739, 2740, 2741, 2742, 2743, 2744, 2745, 2746, 2747, 2748, 2749, 2750, 2751, 2752, 2753, 2754, 2755, 2756, 2757, 2758, 2759, 2760, 2761, 2762, 2763, 2764, 2765, 2766, 2767, 2768, 2769, 2770, 2771, 2772, 2773, 2774, 2775, 2776, 2777, 2778, 2779, 2780, 2781, 2782, 2783, 2784, 2785, 2786, 2787, 2788, 2789, 2790, 2791, 2792, 2793, 2794, 2795, 2796, 2797, 2798, 2799, 2800, 2801, 2802, 2803, 2804, 2805, 2806, 2807, 2808, 2809, 2810, 2811, 2812, 2813, 2814, 2815, 2816, 2817, 2818, 2819, 2820, 2821, 2822, 2823, 2824, 2825, 2826, 2827, 2828, 2829, 2830, 2831, 2832, 2833, 2834, 2835, 2836, 2837, 2838, 2839, 2840, 2841, 2842, 2843, 2844, 2845, 2846, 2847, 2848, 2849, 2850, 2851, 2852, 2853, 2854, 2855, 2856, 2857, 2858, 2859, 2860, 2861, 2862, 2863, 2864, 2865, 2866, 2867, 2868, 2869, 2870, 2871, 2872, 2873, 2874, 2875, 2876, 2877, 2878, 2879, 2880, 2881, 2882, 2883, 2884, 2885, 2886, 2887, 2888, 2889, 2890, 2891, 2892, 2893, 2894, 2895, 2896, 2897, 2898, 2899, 2900, 2901, 2902, 2903, 2904, 2905, 2906, 2907, 2908, 2909, 2910, 2911, 2912, 2913, 2914, 2915, 2916, 2917, 2918, 2919, 2920, 2921, 2922, 2923, 2924, 2925, 2926, 2927, 2928, 2929, 2930, 2931, 2932, 2933, 2934, 2935, 2936, 2937, 2938, 2939, 2940, 2941, 2942, 2943, 2944, 2945, 2946, 2947, 2948, 2949, 2950, 2951, 2952, 2953, 2954, 2955, 2956, 2957, 2958, 2959, 2960, 2961, 2962, 2963, 2964, 2965, 2966, 2967, 2968, 2969, 2970, 2971, 2972, 2973, 2974, 2975, 2976, 2977, 2978, 2979, 2980, 2981, 2982, 2983, 2984, 2985, 2986, 2987, 2988, 2989, 2990, 2991, 2992, 2993, 2994, 2995, 2996, 2997, 2998, 2999, 3000, 3001, 3002, 3003, 3004, 3005, 3006, 3007, 3008, 3009, 3010, 3011, 3012, 3013, 3014, 3015, 3016, 3017, 3018, 3019, 3020, 3021, 3022, 3023, 3024, 3025, 3026, 3027, 3028, 3029, 3030, 3031, 3032, 3033, 3034, 3035, 3036, 3037, 3038, 3039, 3040, 3041, 3042, 3043, 3044, 3045, 3046, 3047, 3048, 3049, 3050, 3051, 3052, 3053, 3054, 3055, 3056, 3057, 3058, 3059, 3060, 3061, 3062, 3063, 3064, 3065, 3066, 3067, 3068, 3069, 3070, 3071, 3072, 3073, 3074, 3075, 3076, 3077, 3078, 3079, 3080, 3081, 3082, 3083, 3084, 3085, 3086, 3087, 3088, 3089, 3090, 3091, 3092, 3093, 3094, 3095, 3096, 3097, 3098, 3099, 3100, 3101, 3102, 3103, 3104, 3105, 3106, 3107, 3108, 3109, 3110, 3111, 3112, 3113, 3114, 3115, 3116, 3117, 3118, 3119, 3120, 3121, 3122, 3123, 3124, 3125, 3126, 3127, 3128, 3129, 3130, 3131, 3132, 3133, 3134, 3135, 3136, 3137, 3138, 3139, 3140, 3141, 3142, 3143, 3144, 3145, 3146, 3147, 3148, 3149, 3150, 3151, 3152, 3153, 3154, 3155, 3156, 3157, 3158, 3159, 3160, 3161, 3162, 3163, 3164, 3165, 3166, 3167, 3168, 3169, 3170, 3171, 3172, 3173, 3174, 3175, 3176, 3177, 3178, 3179, 3180, 3181, 3182, 3183, 3184, 3185, 3186, 3187, 3188, 3189, 3190, 3191, 3192, 3193, 3194, 3195, 3196, 3197, 3198, 3199, 3200, 3201, 3202, 3203, 3204, 3205, 3206, 3207, 3208, 3209, 3210, 3211, 3212, 3213, 3214, 3215, 3216, 3217, 3218, 3219, 3220, 3221, 3222, 3223, 3224, 3225, 3226, 3227, 3228, 3229, 3230, 3231, 3232, 3233, 3234, 3235, 3236, 3237, 3238, 3239, 3240, 3241, 3242, 3243, 3244, 3245, 3246, 3247, 3248, 3249, 3250, 3251, 3252, 3253, 3254, 3255, 3256, 3257, 3258, 3259, 3260, 3261, 3262, 3263, 3264, 3265, 3266, 3267, 3268, 3269, 3270, 3271, 3272, 3273, 3274, 3275, 3276, 3277, 3278, 3279, 3280, 3281, 3282, 3283, 3284, 3285, 3286, 3287, 3288, 3289, 3290, 3291, 3292, 3293, 3294, 3295, 3296, 3297, 3298, 3299, 3300, 3301, 3302, 3303, 3304, 3305, 3306, 3307, 3308, 3309, 3310, 3311, 3312, 3313, 3314, 3315, 3316, 3317, 3318, 3319, 3320, 3321, 3322, 3323, 3324, 3325, 3326, 3327, 3328, 3329, 3330, 3331, 3332, 3333, 3334, 3335, 3336, 3337, 3338, 3339, 3340, 3341, 3342, 3343, 3344, 3345, 3346, 3347, 3348, 3349, 3350, 3351, 3352, 3353, 3354, 3355, 3356, 3357, 3358, 3359, 3360, 3361, 3362, 3363, 3364, 3365, 3366, 3367, 3368, 3369, 3370, 3371, 3372, 3373, 3374, 3375, 3376, 3377, 3378, 3379, 3380, 3381, 3382, 3383, 3384, 3385, 3386, 3387, 3388, 3389, 3390, 3391, 3392, 3393, 3394, 3395, 3396, 3397, 3398, 3399, 3400, 3401, 3402, 3403, 3404, 3405, 3406, 3407, 3408, 3409, 3410, 3411, 3412, 3413, 3414, 3415, 3416, 3417, 3418, 3419, 3420, 3421, 3422, 3423, 3424, 3425, 3426, 3427, 3428, 3429, 3430, 3431, 3432, 3433, 3434, 3435, 3436, 3437, 3438, 3439, 3440, 3441, 3442, 3443, 3444, 3445, 3446, 3447, 3448, 3449, 3450, 3451, 3452, 3453, 3454, 3455, 3456, 3457, 3458, 3459, 3460, 3461, 3462, 3463, 3464, 3465, 3466, 3467, 3468, 3469, 3470, 3471, 3472, 3473, 3474, 3475, 3476, 3477, 3478, 3479, 3480, 3481, 3482, 3483, 3484, 3485, 3486, 3487, 3488, 3489, 3490, 3491, 3492, 3493, 3494, 3495, 3496, 3497, 3498, 3499, 3500, 3501, 3502, 3503, 3504, 3505, 3506, 3507, 3508, 3509, 3510, 3511, 3512, 3513, 3514, 3515, 3516, 3517, 3518, 3519, 3520, 3521, 3522, 3523, 3524, 3525, 3526, 3527, 3528, 3529, 3530, 3531, 3532, 3533, 3534, 3535, 3536, 3537, 3538, 3539, 3540, 3541, 3542, 3543, 3544, 3545, 3546, 3547, 3548, 3549, 3550, 3551, 3552, 3553, 3554, 3555, 3556, 3557, 3558, 3559, 3560, 3561, 3562, 3563, 3564, 3565, 3566, 3567, 3568, 3569, 3570, 3571, 3572, 3573, 3574, 3575, 3576, 3577, 3578, 3579, 3580, 3581, 3582, 3583, 3584, 3585, 3586, 3587, 3588, 3589, 3590, 3591, 3592, 3593, 3594, 3595, 3596, 3597, 3598, 3599, 3600, 3601, 3602, 3603, 3604, 3605, 3606, 3607, 3608, 3609, 3610, 3611, 3612, 3613, 3614, 3615, 3616, 3617, 3618, 3619, 3620, 3621, 3622, 3623, 3624, 3625, 3626, 3627, 3628, 3629, 3630, 3631, 3632, 3633, 3634, 3635, 3636, 3637, 3638, 3639, 3640, 3641, 3642, 3643, 3644, 3645, 3646, 3647, 3648, 3649, 3650, 3651, 3652, 3653, 3654, 3655, 3656, 3657, 3658, 3659, 3660, 3661, 3662, 3663, 3664, 3665, 3666, 3667, 3668, 3669, 3670, 3671, 3672, 3673, 3674, 3675, 3676, 3677, 3678, 3679, 3680, 3681, 3682, 3683, 3684, 3685, 3686, 3687, 3688, 3689, 3690, 3691, 3692, 3693, 3694, 3695, 3696, 3697, 3698, 3699, 3700, 3701, 3702, 3703, 3704, 3705, 3706, 3707, 3708, 3709, 3710, 3711, 3712, 3713, 3714, 3715, 3716, 3717, 3718, 3719, 3720, 3721, 3722, 3723, 3724, 3725, 3726, 3727, 3728, 3729, 3730, 3731, 3732, 3733, 3734, 3735, 3736, 3737, 3738 at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 21805.
WARNING - The following subscriptions are deleted, they were not attached to an existing bibliographic record (subscriptionid): 1, 3, 2 at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 21805.
Upgrade to 19.12.00.076  [21:36:23]: Bug 21901 - Add foreign key constraints on serial
Upgrade to 19.12.00.077  [21:36:23]: Bug 23727 - Editing course reserve items is broken
Upgrade to 19.12.00.078  [21:36:23]: Bug 24913 - Add PatronSelfRegistrationConfirmEmail syspref
Upgrade to 19.12.00.079  [21:36:23]: Bug 25045 - Add a way to restrict anonymous access to public routes (OpacPublic behaviour)
Upgrade to 19.12.00.080  [21:36:23]: Bug 23081 - Set default to 0 for items.issues
Upgrade to 19.12.00.081  [21:36:23]: Bug 22630 - Add course_items.homebranch
Upgrade to 19.12.00.082  [21:36:23]: Bug 23794 - Move contents of OpacMainUserBlock preference to Koha news system
Upgrade to 19.12.00.083  [21:36:23]: Bug 17355 - Add is_system to authorised_value_categories table
Upgrade to 19.12.00.084  [21:36:23]: Bug 17682 - Add macros db table and permissions
Upgrade to 19.12.00.085  [21:36:23]: Bug 24161 - Add new join table aqorders_claims to keep track of claims
Upgrade to 19.12.00.086  [21:36:23]: Bug 24163 - Define a default CSV profile for late orders
Upgrade to 19.12.00.087  [21:36:23]: Bug 25184 - Items with a negative notforloan status should not be captured for holds
Upgrade to 19.12.00.088  [21:36:23]: Bug 24378 - Fix some grammatical errors in default auto renewal notice
Upgrade to 19.12.00.089  [21:36:23]: Bug 25389 - Catch errant cases of LOST_RETURNED
Upgrade to 19.12.00.090  [21:36:23]: Bug 13881 - Add issue desks system preference
Upgrade to 19.12.00.091  [21:36:23]: Bug 13881 - Correction to preference terminology
Upgrade to 20.05.00.000  [21:36:23]: 20.05.00 alpha release
Upgrade to 20.06.00.000  [21:36:23]: All our codebase are belong to everybody
Upgrade to 20.06.00.001  [21:36:25]: Bug 24986 - Switch borrowers address related fields to TINYTEXT or MEDIUMTEXT
Upgrade to 20.06.00.002  [21:36:25]: Bug 25184 - Items with a negative notforloan status should not be captured for holds
Upgrade to 20.06.00.003  [21:36:25]: Bug 24156 - Add new table tables_settings
Upgrade to 20.06.00.004  [21:36:25]: Bug 25851 - Remove holdallowed rule if value is an empty string
Upgrade to 20.06.00.005  [21:36:25]: Bug 24379 - Set login_attempts NOT NULL
Upgrade to 20.06.00.006  [21:36:25]: Bug 24151 - Add pseudonymized_transactions tables and sysprefs for Pseudonymization
Upgrade to 20.06.00.007  [21:36:25]: Bug 22844 - Add borrower_attribute_types.mandatory
Upgrade to 20.06.00.008  [21:36:25]: Bug 23148 - Replace Bridge icons with transparent PNG files
Upgrade to 20.06.00.009  [21:36:25]: Bug 23391 - Hide finished ILL requests
Upgrade to 20.06.00.010  [21:36:25]: Bug 20815 - Add NoRefundOnLostReturnedItemsAge system preference
Upgrade to 20.06.00.011  [21:36:26]: Bug  5087 - Add export_format.staff_only
Upgrade to 20.06.00.012  [21:36:26]: Bug 23795 - Convert OpacCredits system preference to news block
Upgrade to 20.06.00.013  [21:36:26]: Bug 23795 - Convert OpacCustomSearch system preference to news block
Upgrade to 20.06.00.014  [21:36:26]: Bug 23797 - Extend the opac_news lang column to accommodate longer values
Upgrade to 20.06.00.015  [21:36:26]: Bug 23797 - Convert OpacLoginInstructions system preference to news block
Upgrade to 20.06.00.016  [21:36:26]: Bug 23092 - Add 'daterequested' field to transfers table
Upgrade to 20.06.00.017  [21:36:26]: Bug 25709 - Rename systempreference to NotesToHide
Upgrade to 20.06.00.018  [21:36:26]: Bug 24157 - Add new permissions reopen_closed_invoices, edit_invoices, delete_invoices, merge_invoices, delete_basket
Upgrade to 20.06.00.019  [21:36:26]: Bug 22660 - Adds NewsToolEditor system preference
Upgrade to 20.06.00.020  [21:36:26]: Bug 26070 - Remove references to deprecated Google Transliterate API
Upgrade to 20.06.00.021  [21:36:26]: Bug 25871 - Add library option to OPACItemLocation
Upgrade to 20.06.00.022  [21:36:26]: Bug 21946 - Add parent type to itemtypes
Upgrade to 20.06.00.023  [21:36:26]: Bug 16371 - Quote of the Day (QOTD) for the staff interface
Upgrade to 20.06.00.024  [21:36:26]: Bug 25867 - Update subfield descriptions for 952$a and 952$b
Upgrade to 20.06.00.025  [21:36:26]: Bug  6725 - Adds PatronDuplicateMatchingAddFields system preference
Upgrade to 20.06.00.026  [21:36:26]: Bug 19036 - Add accountlines.credit_number, account_credit_types.credit_number_enabled and syspref AutoCreditNumber
Upgrade to 20.06.00.027  [21:36:26]: Bug  8732 - Add new BiblioItemtypeInfo to system preferences
Upgrade to 20.06.00.028  [21:36:26]: Bug 25958 - Allow LongOverdue cron to exclude specified lost values
Upgrade to 20.06.00.029  [21:36:26]: Bug 25534 - Add ability to send an email specifying a reason when canceling a hold
Upgrade to 20.06.00.030  [21:36:26]: Bug 20057 - Add new system preference 'AutoApprovePatronProfileSettings'
Upgrade to 20.06.00.031  [21:36:26]: Bug 22789 - Add non_priority column on reserves and old_reserves tables
Upgrade to 20.06.00.032  [21:36:26]: Bug 19889 - Add exclude_from_local_holds_priority column to items, deleteditems and categories tables
Upgrade to 20.06.00.033  [21:36:26]: Bug 21066 - Rename column opac_news.timestamp with published_on
Upgrade to 20.06.00.034  [21:36:26]: Bug 24197 - Add new system preference 'AddressForFailedOverdueNotices'
Upgrade to 20.06.00.035  [21:36:26]: Bug 23682 - Add new system preference 'EdifactInvoiceImport'
Upgrade to 20.06.00.036  [21:36:26]: Bug 20168 - Update OPACSearchForTitleIn to work with Bootstrap 4
Upgrade to 20.06.00.037  [21:36:26]: Bug 23816 - Add min_password_length and require_strong_password columns in categories table
Upgrade to 20.06.00.038  [21:36:26]: Bug 24807 - Add 'year' type to improve sorting behaviour
Upgrade to 20.06.00.039  [21:36:26]: Bug 18958 - Add reserve_id to hold_fill_targets
Upgrade to 20.06.00.040  [21:36:26]: Bug 26454 - Add system preference to set meta description for the OPAC
Warning - Cannot remove column items.paidfor. At least one value exists at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 22844.
Warning - Cannot remove column deleteditems.paidfor. At least one value exists at /usr/share/koha/intranet/cgi-bin/installer/data/mysql/updatedatabase.pl line 22861.
Upgrade to 20.06.00.041  [21:36:26]: Bug 26268 - Remove items.paidfor field
Upgrade to 20.06.00.042  [21:36:26]: Bug 25776 - Add letter.updated_on
Upgrade to 20.06.00.043  [21:36:26]: Bug 25261 - Add CircConfirmItemParts syspref
Upgrade to 20.06.00.044  [21:36:26]: Bug 22343 - Add SMTP configuration options
Upgrade to 20.06.00.045  [21:36:26]: Bug 22417 - Add new table background_jobs
Upgrade to 20.06.00.046  [21:36:26]: Bug 13535 - Add FK constraint on borrowernumber to alert table
Upgrade to 20.06.00.047  [21:36:26]: Bug 23420 - Allow configuration of hidden fields on the suggestion form in OPAC
Upgrade to 20.06.00.048  [21:36:26]: Bug 26529 - Remove blank default branch rules
Upgrade to 20.06.00.049  [21:36:28]: Bug 26145 - Add the biblioimages.itemnumber column
Upgrade to 20.06.00.050  [21:36:28]: Bug 19382 - Add ability to block guarantees based on fees owed by guarantor and other guarantee - new system preference 'NoIssuesChargeGuarantorsWithGuarantees'
Upgrade to 20.06.00.051  [21:36:28]: Bug 12556 - Add new syspref HoldsNeedProcessingSIP
Upgrade to 20.06.00.052  [21:36:28]: Bug 25460 - Update OAI set when adding/editing/deleting item records
Upgrade to 20.06.00.053  [21:36:28]: Bug 26569 - Use gender neutral pronouns in system preference explanations
Upgrade to 20.06.00.054  [21:36:28]: Bug 25596 - Add OVERPAYMENT credit type
Upgrade to 20.06.00.055  [21:36:28]: Bug 18050 - Add FK constraint on aqbudgets.budget_period_id
Upgrade to 20.06.00.056  [21:36:29]: Bug 26853 - Update import_biblios columns and indexes
Upgrade to 20.06.00.057  [21:36:29]: Bug 26638 - Add missing system preference ArticleRequestsMandatoryFieldsItemOnly
Upgrade to 20.06.00.058  [21:36:29]: Bug 25333 - Change message transport type for Talking Tech from "phone" to "itiva"
Upgrade to 20.06.00.059  [21:36:29]: Bug 19482 - Add mandatory column to search_field for ES mapping
Upgrade to 20.06.00.060  [21:36:29]: Bug 25334 - Add generic 'phone' message transport type
Upgrade to 20.06.00.061  [21:36:29]: Bug 24412 - Attach waiting reserve to desk
Upgrade to 20.06.00.062  [21:36:29]: Bug 23091 - Update refund rules
Upgrade to 20.06.00.063  [21:36:29]: Bug 14866 - Add decreaseloanholds circulation rule
Upgrade to 20.06.00.064  [21:36:29]: Bug 24603 - Add CANCELLATION credit_type_code
Upgrade to 20.06.00.065  [21:36:30]: Bug 23916 - Add new [old_]issues.issuer DB fields
Upgrade to 20.06.00.066  [21:36:30]: Bug 22818 - Add ILL notices
Upgrade to 20.06.00.067  [21:36:30]: Bug 20936 - Add new system preference OPACHoldsHistory
Upgrade to 20.06.00.068  [21:36:30]: Bug 23019 - Add import_batch_profiles table and profile_id column in import_batches
Upgrade to 20.06.00.069  [21:36:30]: Bug 24083 - Add circulation_rules 'unseen_renewals_allowed'
Upgrade to 20.11.00.000  [21:36:30]: Koha 20.11.00 release
Upgrade to 20.12.00.000  [21:36:30]: Sorry, this is my first life, I am still learning!
Upgrade to 20.12.00.001  [21:36:30]: Bug 27252 - Add ElasticsearchCrossFields system preference
Upgrade to 20.12.00.002  [21:36:30]: Bug 27351 - Set type for UsageStatsCountry to Choice
Upgrade to 20.12.00.003  [21:36:30]: Bug 27349 - Update type for Mana system preference to Choice
Upgrade to 20.12.00.004  [21:36:30]: Bug 27485 - Rename system preference 'gist' to 'TaxRates'
Upgrade to 20.12.00.005  [21:36:30]: Bug 27491 - Rename system preference 'opaclanguages' to 'OPACLanguages'
Upgrade to 20.12.00.006  [21:36:30]: Bug 27487 - Rename system preference 'reviewson' to 'OPACComments
Upgrade to 20.12.00.007  [21:36:30]: Bug 27486 - Renaming system preference 'delimiter' to 'CSVDelimiter'
Upgrade to 20.12.00.008  [21:36:30]: Bug 25552 - Add missing Claims Returned option to MarkLostItemsAsReturned
Upgrade to 20.12.00.009  [21:36:30]: Bug 27581 - Rename system preference 'UseICU' to 'UseICUStyleQuotes'
Upgrade to 20.12.00.010  [21:36:30]: Bug 20410 - Remove OpacGroupResults
Upgrade to 20.12.00.011  [21:36:30]: Bug 18506 - Add OPACShibOnly and staffShibOnly system preferences
Upgrade to 20.12.00.012  [21:36:30]: Bug 27598 - Add UPLOAD as a built-in system authorized value category
Upgrade to 20.12.00.013  [21:36:30]: Bug 24108 - Add system preference DefaultSaveRecordFileID
Upgrade to 20.12.00.014  [21:36:30]: Bug  7806 - Remove remaining possible 0000-00-00 values
Upgrade to 20.12.00.015  [21:36:30]: Bug 27316 - In Elastisearch mappings convert NULL (Undef) for sort to 1 (Yes)
Upgrade to 20.12.00.016  [21:36:30]: Bug  8976 - Allow setting a default sequence of subfields in cataloguing editor
Upgrade to 20.12.00.017  [21:36:30]: Bug 26937 - Add CheckPrevCheckoutDelay system preference)
Upgrade to 20.12.00.018  [21:36:30]: Bug 27808 - Adjust items.onloan if needed
Upgrade to 20.12.00.019  [21:36:30]: Bug 26057 - Add datecancelled field to branchtransfers
Upgrade to 20.12.00.020  [21:36:30]: Bug 24446 - Update stockrotation 'daterequested' field in transfers table
Upgrade to 20.12.00.021  [21:36:30]: Bug 22824 - Update syspref values for YesNo
Upgrade to 20.12.00.022  [21:36:30]: Bug 12224 - Add CHECKINSLIP notice
Upgrade to 20.12.00.023  [21:36:30]: Bug 27652 - Separate values for OPACHoldsIfAvailableAtPickupExceptions and BatchCheckoutsValidCategories with comma
Upgrade to 20.12.00.024  [21:36:30]: Bug 18532 - Messaging preferences for auto renewals
Upgrade to 20.12.00.025  [21:36:30]: Bug 27835 - Add new system preference ChargeFinesOnClosedDays
Upgrade to 20.12.00.026  [21:36:30]: Bug 26498 - Bug 26498 - Add option to set a default expire date for holds at reservation time
Upgrade to 20.12.00.027  [21:36:30]: Bug 27069 - Change holdallowed values from numbers to strings
Upgrade to 20.12.00.028  [21:36:30]: Bug 14233 - Add id field to letter table
Upgrade to 20.12.00.029  [21:36:30]: Bug 27726 - Increase field size for problem_reports.content
Upgrade to 20.12.00.030  [21:36:30]: Bug 21549 - Add new system preference LockExpiredDelay
Upgrade to 20.12.00.031  [21:36:30]: Bug 21260 - Add new system preference Reference_NFL_Statuses
Upgrade to 20.12.00.032  [21:36:30]: Bug 15986 - Add sample HOLD_REMINDER notice
Upgrade to 20.12.00.033  [21:36:30]: Bug 26940 - Put in sync borrowers.debarredcomment with comments from borrower_debarments
Upgrade to 20.12.00.034  [21:36:30]: Bug 20854 - Add new system preference casServerVersion
Upgrade to 20.12.00.035  [21:36:30]: Bug 23207 - Add automatic_checkin to itemtypes table
Upgrade to 20.12.00.036  [21:36:30]: Bug 16787 - Add noReservesAllowed to club holds error codes
Upgrade to 20.12.00.037  [21:36:30]: Bug 23971 - Add new system preference AcquisitionLog
Upgrade to 20.12.00.038  [21:36:30]: Bug 27281 - Add 'ItemLost' to branchtransfers.cancellation_reason enum
Upgrade to 20.12.00.039  [21:36:30]: Bug 12362 - Add 'TransferCancellation' to branchtransfers.reason enum
Upgrade to 20.12.00.040  [21:36:30]: Bug 27971 - Add VOID debit type code
Upgrade to 20.12.00.041  [21:36:30]: Bug 26734 - Update notices to use defaults
Upgrade to 20.12.00.042  [21:36:30]: Bug 17202 - Add FK constraint for collection to collections_tracking
Upgrade to 20.12.00.043  [21:36:30]: Bug 28258 - Update AUTO_RENEWAL content
Upgrade to 20.12.00.044  [21:36:30]: Bug 28244 - Fix Ukrainian typo in English
Upgrade to 20.12.00.045  [21:36:30]: Bug 21249 - Adding new system preference SearchLimitLibrary
Upgrade to 20.12.00.046  [21:36:30]: Bug 14723 - Additional delivery notes to messages
Upgrade to 20.12.00.047  [21:36:30]: Bug 23215 - Remove core PayPal support in favor of the use of plugins
Upgrade to 20.12.00.048  [21:36:30]: Bug 26995 - [SKIP] Drop column relationship from borrower tables [not executed]
Upgrade to 20.12.00.049  [21:36:30]: Bug 28108 - Move action logs 'SERIAL CLAIM' and 'ACQUISITION CLAIM' to a new 'CLAIMS' module
Upgrade to 20.12.00.050  [21:36:30]: Bug 28108 - Add new systempreference OpacHiddenItemsHidesRecord
Upgrade to 21.05.00.000  [21:36:30]: Koha 21.05.00 release
Upgrade to 21.06.00.000  [21:36:30]: Increase DBRev for 21.06
        🎵 Run, rabbit run. 🎶
        Dig that hole, forget the sun,
        And when at last the work is done
        Don't sit down it's time to dig another one.
Upgrade to 21.06.00.001  [21:36:30]: Bug 28489 - Modify sessions.a_session from longtext to longblob
Upgrade to 21.06.00.002  [21:36:30]: Bug 28490 - Bring back accidentally deleted relationship columns
Upgrade to 21.06.00.003  [21:36:30]: Bug 24434 - Add 'WrongTransfer' to branchtransfers.cancellation_reason enum
Upgrade to 21.06.00.004  [21:36:30]: Bug 15788 - Split edit_borrowers permission
Upgrade to 21.06.00.005  [21:36:30]: Bug 26205 - Add new system preference NewsLog to log news changes
Upgrade to 21.06.00.006  [21:36:30]: Bug 14237 - Add individual bibliographic records to course reserves
        Add course_items.biblionumber column
        Add fk_course_items_biblionumber constraint
        Change course_items.itemnumber to allow NULL values
Upgrade to 21.06.00.007  [21:36:31]: Bug 11879 - Add a new field to patron record: main contact method
Upgrade to 21.06.00.008  [21:36:31]: Bug 20310 - Add new system preference ArticleRequestsOpacHostRedirection
Upgrade to 21.06.00.009  [21:36:31]: Bug 20472 - Add columns format and urls in article_requests table
Upgrade to 21.06.00.010  [21:36:31]: Bug 20472 - Add new system preference ArticleRequestsSupportedFormats
Upgrade to 21.06.00.011  [21:36:31]: Bug 28567 - Set to NULL empty branches fields
Upgrade to 21.06.00.012  [21:36:31]: Bug 15067 - Add missing languages
Upgrade to 21.06.00.013  [21:36:31]: Bug 22435 - Update existing offsets
Upgrade to 21.06.00.014  [21:36:31]: Bug 28813 - Update delivery_note to failure_code in message_queue
Upgrade to 21.06.00.015  [21:36:31]: Bug 12561 - Remove system preferences HighlightOwnItemsOnOPAC and HighlightOwnItemsOnOPACWhich
Upgrade to 21.06.00.016  [21:36:31]: Bug 24387 - Rename opac_news with additional_contents
Upgrade to 21.06.00.017  [21:36:31]: Bug 28872 - Update syspref values from on and off to 1 and 0
Upgrade to 21.06.00.018  [21:36:33]: Bug 22690 - Add contraints to the linktracker table
Upgrade to 21.06.00.019  [21:36:33]: Bug 26302 - Add system preferences OPACResultsMaxItems and OPACResultsMaxItemsUnavailable
Upgrade to 21.06.00.020  [21:36:33]: Bug 28373 - Add new system preference PassItemMarcToXSLT
        NOTE: You have defined a custom stylesheet for 'OPACXSLTDetailsDisplay'. If it is utilizing item fields you must enable the system preference 'PassItemMarcToXSLT'
Upgrade to 21.06.00.021  [21:36:33]: Bug 28774 - Delete blank rental discounts
Upgrade to 21.06.00.022  [21:36:33]: Bug 28972 - Add missing foreign key constraints to holds queue table
Upgrade to 21.06.00.023  [21:36:33]: Bug 28534 - Set pending_offline_operations INNoDB rather than MyISAM
Upgrade to 21.06.00.024  [21:36:33]: Bug 29073 - Make DefaultHoldExpirationdate use 1/0 values
Upgrade to 21.06.00.025  [21:36:33]: Bug 28826 - A system preference FacetOrder
Upgrade to 21.06.00.026  [21:36:33]: Bug 28772 - Store hashed API key secrets
Upgrade to 21.06.00.027  [21:36:33]: Bug 29137 - Add system preference CreateAVFromCataloguing
Upgrade to 21.06.00.028  [21:36:33]: Bug 27944 - Add REQUESTED as enum element for status column, move AR_PENDING letter to AR_REQUESTED, and add new AR_PENDING letter
Upgrade to 21.06.00.029  [21:36:33]: Bug 27947 - Add authorised values list in article requests cancellation
        Add AR_CANCELLATION category for authorised values
        Add AR_CANCELLATION authorised values
        Add cancellation_reason column in article_requests table
        Replace notes by reason in notice AR_CANCELED
Upgrade to 21.06.00.030  [21:36:33]: Bug 25429 - Add new system preference CleanUpDatabaseReturnClaims
Upgrade to 21.06.00.031  [21:36:33]: Bug 18984 - Remove NORMARC from search_marc_map.marc_type
Upgrade to 21.06.00.032  [21:36:33]: Bug 29138 - Use a zero instead of a 'no' in LoadSearchHistoryToTheFirstLoggedUser
Upgrade to 21.06.00.033  [21:36:33]: Bug 29093 - Add column article_requests.toc_request
Upgrade to 21.06.00.034  [21:36:33]: Bug 28831 - Add system preferences OPACResultsUnavailableGroupingBy
Upgrade to 21.06.00.035  [21:36:33]: Bug 28153 - Add Hold Reminder messaging preference
        Message attribute added
        HOLD_REMINDER added to message_transports
        Hold_Filled message preference copied to Hold_Reminder
        Hold_Filled message transport preferences copied to Hold_Reminder
Upgrade to 21.06.00.036  [21:36:33]: Bug 29200 - Remove Adlibris cover service integration
        AdlibrisCoversEnabled and AdlibrisCoversURL preferences removed.
Upgrade to 21.06.00.037  [21:36:33]: Bug 11175 - Show component records in detail views
Upgrade to 21.06.00.038  [21:36:33]: Bug 14957 - Add a way to define overlay rules for incoming MARC records
        Added new table 'marc_overlay_rules'
        Added new system preferences 'MARCOverlayRules'
        Added new permissions 'manage_marc_overlay_rules'
Upgrade to 21.06.00.039  [21:36:33]: Bug 28959 - virtualshelves.category is really a boolean
Upgrade to 21.06.00.040  [21:36:33]: Bug 28263 - Update AUTO_RENEWAL too_many message
Upgrade to 21.06.00.041  [21:36:33]: Bug 27360 - Make display of libraries configurable
Upgrade to 21.06.00.042  [21:36:33]: Bug 26326 - Add primary key to import_record_matches
Upgrade to 21.06.00.043  [21:36:33]: Bug 29386 - Extend background_jobs.data to LONGTEXT
Upgrade to 21.06.00.044  [21:36:33]: Bug 29180 - Rename system preference RequestOnOpac with OPACHoldRequests
Upgrade to 21.06.00.045  [21:36:33]: Bug 24223 - Move contents of OpacNav system preference into additional contents
Upgrade to 21.06.00.046  [21:36:33]: Bug 24224 - Move contents of OpacNavBottom system preference into additional contents
        No OpacNavBottom preference found. Update has already been run.
Upgrade to 21.06.00.047  [21:36:33]: Bug 28374 - Update point of sale print receipt
        Added KohaDates, Branches and Price plugins
        Replaced 'payment' with 'credit' param in RECEIPT template
        Replaced 'offsets' with 'credit.debits' param in RECEIPT template
        Replaced 'offset' with 'debit' param in RECEIPT template
        Replaced 'debit.debit' with 'debit' param in RECEIPT template
Upgrade to 21.06.00.048  [21:36:33]: Bug 29341 - Remove foreign keys on pseudonymized_transactions
Upgrade to 21.06.00.049  [21:36:33]: Bug  5229 - Remove system preference 'OPACItemsResultsDisplay'
Upgrade to 21.11.00.000  [21:36:33]: Koha 21.11.00 release
Upgrade to 21.12.00.000  [21:36:33]: Increase DBRev for 21.12
        📜 All that is gold does not glitter,
        📜 Not all those who wander are lost;
        📜 The old that is strong does not wither,
        📜 Deep roots are not reached by the frost.
Upgrade to 21.12.00.001  [21:36:33]: Bug 29586 - Add Hold Reminder messaging preference if missing
Upgrade to 21.12.00.002  [21:36:33]: Bug 13188 - Allow configuration of required fields when a patron is editing their information via the OPAC
        Added new system preference 'PatronSelfModificationMandatoryField' with value 'surname|firstname|address'
Upgrade to 21.12.00.003  [21:36:33]: Bug 29457 - Fee Cancellation records the wrong manager_id
        WARNING: You may have some incorrect manager_id's recorded against account cancellation lines, please see bugzilla for details.
        NOTE: You may already have this bugfix applied at an earlier upgrade.
Upgrade to 21.12.00.004  [21:36:33]: Bug 26296 - Replace comma with pipe in OPACSuggestion field preferences
Upgrade to 21.12.00.005  [21:36:33]: Bug 29778 - Delete orphan additional contents
Upgrade to 21.12.00.006  [21:36:33]: Bug 29557 - Add auto_account_expired to AUTO_RENEWALS notice
        Please update your AUTO_RENEWALS notice manually if you have changed or translated it
Upgrade to 21.12.00.007  [21:36:33]: Bug 20076 - Add system preference EmailOverduesNoEmail
Upgrade to 21.12.00.008  [21:36:33]: Bug 29495 - Drop issue_id constraint from return_claims table
Upgrade to 21.12.00.009  [21:36:33]: Bug 29336 - Resize authorised value category fields to 32 chars
Upgrade to 21.12.00.010  [21:36:33]: Bug 21729 - Add new column reserves.patron_expiration_date
Upgrade to 21.12.00.011  [21:36:33]: Bug 27946 - Add article request fees
Upgrade to 21.12.00.012  [21:36:33]: Bug 24220 - Move OpacMoreSearches to additional contents
        No OpacMoreSearches preference found. Value was empty or update has already been run.
Upgrade to 21.12.00.013  [21:36:34]: Bug 29605 - Resync DB structure for existing installations
        Added missing primary key on language_script_mapping
        Ensure NOT NULL on account_offsets.type
        Ensure additional_contents.code is VARCHAR(100)
        Ensure additional_contents.lang is VARCHAR(50)
        Ensure NOT NULL on search_marc_map.marc_type
        Ensure branchtransfers.cancellation_reason enum values are uppercase
Upgrade to 21.12.00.014  [21:36:34]: Bug 29596 - Add Yiddish language
Upgrade to 21.12.00.015  [21:36:34]: Bug 29943 - Fix typo in NOTIFY_MANAGER notice
Upgrade to 21.12.00.016  [21:36:34]: Bug 30060 - Update user_permissions to add primary key and remove null option from code column
        Removed any duplicate rows
        ERROR: {UNKNOWN}: DBI Exception: DBD::mysql::db do failed: Cannot add or update a child row: a foreign key constraint fails (`koha_library`.`#sql-alter-100-39`, CONSTRAINT `user_permissions_ibfk_2` FOREIGN KEY (`module_bit`, `code`) REFERENCES `permissions` (`module_bit`, `code`) ON DELETE CASCADE ON UPDATE CASCADE) at /usr/share/koha/lib/C4/Installer.pm line 743
```

## Version 21.1200015 to 23.0600052

```
Upgrade to 21.12.00.016  [21:41:47]: Bug 30060 - Update user_permissions to add primary key and remove null option from code column
Upgrade to 21.12.00.017  [21:41:47]: Bug 30128 - Change language_subtag_registry.description to varchar(255)
Upgrade to 21.12.00.018  [21:41:47]: Bug 19532 - Add Recalls
Upgrade to 21.12.00.019  [21:41:47]: Bug 27812 - Remove the ability to transmit a patron's plain text password over email
        The notice template ACCTDETAILS no longer has access to the patron's plain text password. Please update the language of your ACCTDETAILS as needed.
Upgrade to 21.12.00.020  [21:41:47]: Bug 24221 - Move OpacMySummaryNote to additional contents
        No OpacMySummaryNote preference found. Value was empty or update has already been run.
Upgrade to 21.12.00.021  [21:41:47]: Bug 30063 - Fix DefaultPatronSearchFields order
Upgrade to 21.12.00.022  [21:41:47]: Bug 11083 - Add syspref AuthorityXSLTResultsDisplay
Upgrade to 21.12.00.023  [21:41:47]: Bug 20517 - Add SIP2SortBinMapping system preference
Upgrade to 21.12.00.024  [21:41:47]: Bug 20398 - Add system preference StaffHighlightedWords
Upgrade to 21.12.00.025  [21:41:47]: Bug 29990 - Add new system preference ShowHeadingUse
Upgrade to 21.12.00.026  [21:41:47]: Bug 17018 - Split AdvancedSearchTypes for staff and OPAC
Upgrade to 21.12.00.027  [21:41:47]: Bug 26346 - Add allow_change_from_staff to virtualshelves table
Upgrade to 21.12.00.028  [21:41:47]: Bug 16258 - A preference to enabled/disable edifact
Upgrade to 21.12.00.029  [21:41:47]: Bug 30130 - A standard to edi_account
Upgrade to 21.12.00.030  [21:41:47]: Bug 30135 - Add EdifactLSQ mapping system preference
Upgrade to 21.12.00.031  [21:41:47]: Bug 30481 - DB schema sync for deleteditems
Upgrade to 21.12.00.032  [21:41:47]: Bug 30498 - Correct enum search_field.type
Upgrade to 21.12.00.033  [21:41:47]: Bug 27783 - Add background_jobs.queue
        Added background_jobs.queue
Upgrade to 21.12.00.034  [21:41:47]: Bug 30237 - Replace ACCDETAILS notice with WELCOME notice
Upgrade to 21.12.00.035  [21:41:47]: Bug 30226 - Add the system preference AllowSetAutomaticRenewal
Upgrade to 21.12.00.036  [21:41:47]: Bug 28786 - Add syspref TwoFactorAuthentication, fields secret and auth_method
Upgrade to 21.12.00.037  [21:41:48]: Bug 27253 - Fix definition of borrowers.updated_on and deletedborrowers.updated_on
        Updated all NULL values of borrowers.updated_on to GREATEST(date_renewed, dateenrolled, lastseen): 48 rows updated
        Updated all NULL values of borrowers.updated_on to GREATEST(date_renewed, dateenrolled, lastseen): 11 rows updated
        Fixed definition of borrowers.updated_on
        Fixed definition of deletedborrowers.updated_on
Upgrade to 21.12.00.038  [21:41:48]: Bug 29648 - Move NumSavedReports to table settings and allow tables_settings.default_display_length to be NULL
        NumSavedReports value '20' moved to table settings
Upgrade to 21.12.00.039  [21:41:48]: Bug 29092 - Add timestamp to account-fines table column settings
Upgrade to 21.12.00.040  [21:41:48]: Bug 30565 - Update table stockrotationrotas
Upgrade to 21.12.00.041  [21:41:48]: Bug 30449 - Check borrower_attribute_types FK constraint
Upgrade to 21.12.00.042  [21:41:48]: Bug 30572 - Adjust search_marc_to_field.sort
Upgrade to 21.12.00.043  [21:41:48]: Bug 30108 - Add preference OPACMandatoryHoldDates
Upgrade to 21.12.00.044  [21:41:48]: Bug 29894 - Add 2FA (de)enabling notices
Upgrade to 21.12.00.045  [21:41:48]: Bug 14242 - Add OPACSuggestionAutoFill system preference
Upgrade to 21.12.00.046  [21:41:48]: Bug 22785 - Add chosen column to import_record_matches
        chosen column added to import_record_matches
Upgrade to 21.12.00.047  [21:41:48]: Bug 28138 - Add system preference RequirePaymentType
Upgrade to 21.12.00.048  [21:41:48]: Bug 30291 - Renaming recalls table columns
Upgrade to 21.12.00.049  [21:41:48]: Bug 30563 - Add system preference RequireCashRegister
Upgrade to 21.12.00.050  [21:41:48]: Bug 29924 - Add password expiration
        Added password_expiry_days to categories
        Added password_expiration_date field to borrowers
        Added password_expiration_date field to borrowers
Upgrade to 21.12.00.051  [21:41:48]: Bug 29925 - Add password reset option
Upgrade to 21.12.00.052  [21:41:48]: Bug 30290 - Modify AR notices, include TOC line
Upgrade to 21.12.00.053  [21:41:48]: Bug 30611 - Add STAFF_PASSWORD_RESET notice
Upgrade to 21.12.00.054  [21:41:48]: Bug 23352 - Adding new column 'subscription.ccode'
Upgrade to 21.12.00.055  [21:41:48]: Bug 13412 - Add GenerateAuthorityField667 and GenerateAuthorityField670 system preferences
Upgrade to 21.12.00.056  [21:41:48]: Bug 30728 - Allow opting out of real-time holds queue updating possible
Upgrade to 21.12.00.057  [21:41:48]: Bug 30852 - Add index to article_requests.debit_id
Upgrade to 22.05.00.000  [21:41:48]: Koha 22.05.00 release
Upgrade to 22.06.00.000  [21:41:48]: Increase DBRev for 22.06
        📜 The road of excess
        📜 leads to the palace of wisdom;
        📜 for we never know what is enough
        📜 until we know what is more than enough.
Upgrade to 22.06.00.001  [21:41:48]: Bug 23659 - Allow hold pickup location to default to item home branch for item-level holds
        Added new system preference 'DefaultHoldPickupLocation'
Upgrade to 22.06.00.002  [21:41:48]: Bug 30850 - Message about mappings changes for 110$a
        110$a was added as a default mapping for biblio.author in MARC21. This will only change the mapping on new installations. If you wish to change the mappings on your existing installation, go to Administration > Koha to MARC mapping and add 110$a to biblio.author and then run batchRebuilBiblioTables.pl.
Upgrade to 22.06.00.003  [21:41:48]: Bug 30924 - Add missing RecallCancellation option to branchtransfers.reason ENUM
Upgrade to 22.06.00.004  [21:41:48]: Bug 12446 - Ability to allow guarantor relationship for all patron category types
        Added column 'categories.can_be_guarantee'
Upgrade to 22.06.00.005  [21:41:48]: Bug 24239 - Let the ILL module set ad hoc hard due dates
        Added column 'illrequests.due_date'
Upgrade to 22.06.00.006  [21:41:48]: Bug 21978 - Add middle_name to borrowers table
        Added column 'borrowers.middle_name'
        Added column 'deletedborrowers.middle_name'
        Added column 'borrower_modifications.middle_name'
        Added middle name to DefaultPatronSearchFields
Upgrade to 22.06.00.007  [21:41:48]: Bug 29129 - Update the DisplayClearnScreenButton system pref to allow for a choice between ISSUESLIP and ISSUEQSLIP
Upgrade to 22.06.00.008  [21:41:48]: Bug 30327 - Sort component parts
        Added new system preference 'ComponentSortField'
        Added new system preference 'ComponentSortOrder'
Upgrade to 22.06.00.009  [21:41:48]: Bug 30889 - Add calling context information to background_jobs
        Added column 'background_jobs.context'
Upgrade to 22.06.00.010  [21:41:48]: Bug 30823 - Replace recalls FULFILL actions with FILL in action logs
Upgrade to 22.06.00.011  [21:41:48]: Bug 30275 - Add a checkout_renewals table
        Added new table 'checkout_renewals'
        Renamed `issues.renewals` to `issues.renewals_count`
        Renamed `old_issues.renewals` to `old_issues.renewals_count`
Upgrade to 22.06.00.012  [21:41:48]: Bug 24010 - Make subscription.staffdisplaycount and opacdisplaycount integer columns
Upgrade to 22.06.00.013  [21:41:48]: Bug 24865 - Customize the Accountlines Description
        Added new letter 'OVERDUE_FINE_DESC' (print)
Upgrade to 22.06.00.014  [21:41:48]: Bug 24857 - Add ability to group items on a record
        Added new system preference 'EnableItemGroups'
        Added new permission 'manage_item_groups'
        Added new table 'item_groups'
        Added new table 'item_group_items'
Upgrade to 22.06.00.015  [21:41:48]: Bug 28854 - Item bundles support
        Added new table 'item_bundles'
        Missing from bundle LOST AV added
        Added to bundle NOT_LOAN AV added
        Added new system preference 'BundleLostValue'
        Added new system preference 'BundleNotLoanValue'
        Dropped unique constraint on issue_id in return_claims
Upgrade to 22.06.00.016  [21:41:48]: Bug 28854 - Add new 'item_issue' unique index to return claims
Upgrade to 22.06.00.017  [21:41:48]: Bug 29632 - Add callnumber type to allow sorting
        Add callnumber to search_field type enum
Upgrade to 22.06.00.018  [21:41:48]: Bug 11889 - Add option to keep public or shared lists when deleting patron
        Added new system preference 'ListOwnershipUponPatronDeletion'
Upgrade to 22.06.00.019  [21:41:48]: Bug 30933 - Add a designated owner for shared and public lists at patron deletion
        Added new system preference 'ListOwnerDesignated'
        Updated system preference 'ListOwnershipUponPatronDeletion'
Upgrade to 22.06.00.020  [21:41:48]: Bug 31086 - Do not allow NULL values in branchcodes for reserves
        Removed NULL option from branchcode for reserves
Upgrade to 22.06.00.021  [21:41:49]: Bug 31157 - Make --frombranch option (overdue_notices.pl) available as a syspref
        Added new system preference 'OverdueNoticeFrom'
Upgrade to 22.06.00.022  [21:41:49]: Bug 30650 - Add Curbside pickup feature
        Added new table 'curbside_pickup_policy'
        Added new table 'curbside_pickup_opening_slots'
        Added new table 'curbside_pickups'
        Added new table 'curbside_pickup_issues'
        Added new letter 'NEW_CURBSIDE_PICKUP' (email)
        Added new system preference 'CurbsidePickup'
        Added new permission 'manage_curbside_pickups' (circulation)
        Added new permission 'manage_curbside_pickups' (admin)
        Added column 'curbside_pickup_policy.enable_waiting_holds_only'
Upgrade to 22.06.00.023  [21:41:49]: Bug 22456 - Allow cancelling waiting holds
        Added new table 'hold_cancellation_requests'
Upgrade to 22.06.00.024  [21:41:49]: Bug 29012/33847 - Some rules are not saved when left blank while editing a 'rule' line in smart-rules.pl
        Set derived values for blank circulation rules that weren't saved to the database
Upgrade to 22.06.00.025  [21:41:49]: Bug 14364 - Allow automatically canceled expired waiting holds to fill the next hold
        Added new system preference 'ExpireReservesAutoFill'
        Added new letter 'HOLD_CHANGED' (email)
Upgrade to 22.06.00.026  [21:41:49]: Bug 30984 - Log the cron script that generated an action log if there is one
        Added column 'action_logs.script'
Upgrade to 22.06.00.027  [21:41:49]: Bug 28269 - Make it possible to search orders with ISSN
        Added new system preference 'SearchWithISSNVariations'
Upgrade to 22.06.00.028  [21:41:49]: Bug 30077 - Add option for library dropdown in search function for staff interface
        Added new system preference 'IntranetAddMastheadLibraryPulldown'
Upgrade to 22.06.00.029  [21:41:49]: Bug 30392 - Add deleteditems.deleted_on
Upgrade to 22.06.00.030  [21:41:49]: Bug 31274 - OPACSuggestionAutoFill must be 1 or 0
        Updated system preference 'OPACSuggestionAutoFill'
Upgrade to 22.06.00.031  [21:41:49]: Bug 30327 - Add biblionumber to ComponentSortField
        Added biblionumber option to ComponentSortField
Upgrade to 22.06.00.032  [21:41:49]: Bug 30500 - Add option to allow user to change the pickup location while a hold is in transit
        Added new system preference 'OPACInTransitHoldPickupLocationChange'
Upgrade to 22.06.00.033  [21:41:49]: Bug 27779 - Simplify credit descriptions
Upgrade to 22.06.00.034  [21:41:49]: Bug 29897 - Display author identifiers for researchers
        Added new system preference 'OPACAuthorIdentifiers'
Upgrade to 22.06.00.035  [21:41:49]: Bug 28787 - Send a notice with the TOTP token
        Added new letter '2FA_OTP_TOKEN' (email)
Upgrade to 22.06.00.036  [21:41:49]: Bug 31017 - Add type option to vendors
        Added column 'aqbooksellers.type'
        Added VENDOR_TYPE authorised value category
Upgrade to 22.06.00.037  [21:41:49]: Bug 23681 - Add customisable patron restriction types
        Added new table 'restriction_types'
        Added system restriction_types
        Added borrower_debarments relation
        Added new permission 'manage_patron_restrictions'
        Added new system preference 'PatronRestrictionTypes'
Upgrade to 22.06.00.038  [21:41:49]: Bug 30335 - Add manual_invoice and manual_credit permissions
        Added new permission 'manual_credit'
        Added new permission 'manual_invoice'
Upgrade to 22.06.00.039  [21:41:49]: Bug 31374 - Add a non-public note column to the suggestions table
        Added column 'suggestions.staff_note'
Upgrade to 22.06.00.040  [21:41:49]: Bug 30619 - Add email notice for Point of Sale > RECEIPT
        Added new letter 'RECEIPT' (email)
Upgrade to 22.06.00.041  [21:41:49]: Bug 30483 - Make issues.borrowernumber and issues.itemnumber NOT NULL
Upgrade to 22.06.00.042  [21:41:49]: Bug 27981 - Make it possible to force 001 = biblionumber
        Added new system preference 'autoControlNumber'
Upgrade to 22.06.00.043  [21:41:49]: Bug 20058 - Option to use shelving location instead of homebranch for sorting
        Added new system preference 'UseLocationAsAQInSIP'
Upgrade to 22.06.00.044  [21:41:49]: Bug 26247 - Add new retain search terms preferences
        Added new system preference 'RetainCatalogSearchTerms'
        Added new system preference 'RetainPatronsSearchTerms'
Upgrade to 22.06.00.045  [21:41:49]: Bug 29144 - Copy and remove branches.opac_info
Upgrade to 22.06.00.046  [21:41:49]: Bug 15348 - Add new column aqorders.estimated_delivery_date
Upgrade to 22.06.00.047  [21:41:49]: Bug 30025 - Split and rename BiblioAddsAuthorities system preference
        Added new system preference 'RequireChoosingExistingAuthority'
        Added new system preference 'AutoLinkBiblios'
        Removed system preference 'BiblioAddsAuthorities'
Upgrade to 22.06.00.048  [21:41:49]: Bug 30472 - borrower_relationships.guarantor_id NOT NULL
Upgrade to 22.06.00.049  [21:41:49]: Bug 30490 - Adjust FK constraint for parent item type
Upgrade to 22.06.00.050  [21:41:49]: Bug 30497 - Recreate old_reserves_ibfk_4 if cascading
Upgrade to 22.06.00.051  [21:41:49]: Bug  7021 - Add patron category to the statistics table
        Added column 'statistics.categorycode'
Upgrade to 22.06.00.052  [21:41:49]: Bug 25735 - Add Elasticsearch field 'available'
Upgrade to 22.06.00.053  [21:41:49]: Bug 30484 - Add a notice template for ILL Update notices
        Added new letter 'ILL_REQUEST_UPDATE' (email)
        Added new letter 'ILL_REQUEST_UPDATE' (sms)
Upgrade to 22.06.00.054  [21:41:49]: Bug 23538 - Add new system preferences EmailPatronRegistrations and EmailAddressForPatronRegistrations and new OPAC_REG letter
        Added new system preference 'EmailPatronRegistrations'
        Added new letter 'OPAC_REG' (email)
Upgrade to 22.06.00.055  [21:41:49]: Bug 26368 - Add OCLC Encoding Levels system preference
        Added new system preference 'UseOCLCEncodingLevels'
Upgrade to 22.06.00.056  [21:41:49]: Bug 30571 - Table z3950servers: three cols NOT NULL
Upgrade to 22.06.00.057  [21:41:49]: Bug 29071 - Set HoldsQueueSplitNumbering where not set
        Added new system preference 'HoldsSplitQueueNumbering'
Upgrade to 22.06.00.058  [21:41:49]: Bug 30944 - Replace branchtransfers.cancellation_reason CancelRecall with RecallCancellation
Upgrade to 22.06.00.059  [21:41:49]: Bug 25936 - A password change notification feature
        Added new letter 'PASSWORD_CHANGE' (email)
        Added new system preference 'NotifyPasswordChange'
Upgrade to 22.06.00.060  [21:41:49]: Bug 10950 - Add preferred pronoun field to patron record
        Added column 'borrowers.pronouns'
        Added column 'deletedborrowers.pronouns'
        Added column 'borrower_modifications.pronouns'
Upgrade to 22.06.00.061  [21:41:49]: Bug 31333 - Add the ability to limit purchase suggestions by patron category
        Added new system preference 'suggestionPatronCategoryExceptions'
Upgrade to 22.06.00.062  [21:41:49]: Bug 27136 - Add missing languages: Cree, Afrikaans and Multiple languages, Undetermined and No linguistic content
        Added missing languages
Upgrade to 22.06.00.063  [21:41:50]: Bug 31569 - Add primary key for import_biblios
        Added primary key to import_biblios table
Upgrade to 22.06.00.064  [21:41:50]: Bug 14783 - Allow patrons to change pickup location for non-waiting holds
        Added new system preference 'OPACAllowUserToChangeBranch'
        Removed system preference 'OPACInTransitHoldPickupLocationChange'
Upgrade to 22.06.00.065  [21:41:50]: Bug 25426 - Add new syspref CircControlReturnsBranch
        Added new system preference 'CircControlReturnsBranch'
Upgrade to 22.06.00.066  [21:41:50]: Bug 31626 - Add letter id to the message queue table
        Added column 'message_queue.letter_id'
Upgrade to 22.06.00.067  [21:41:50]: Bug 17170 - Add saved search filters feature
        Added new permission 'manage_search_filters'
        Added new table 'search_filters'
        Added new system preference 'SavedSearchFilters'
Upgrade to 22.06.00.068  [21:41:50]: Bug 30588 - Add an 'enforce' option for 'TwoFactorAuthentication' system preference
        Updated system preference 'TwoFactorAuthentication'
Upgrade to 22.06.00.069  [21:41:50]: Bug 31715 - Add missing German (de) language translations
        German (de) translations were added
Upgrade to 22.06.00.070  [21:41:50]: Bug 31577 - Add category list pull-down to OpacHiddenItemsExceptions
        Updated system preference 'OpacHiddenItemsExceptions'
Upgrade to 22.06.00.071  [21:41:50]: Bug 23012 - Add PROCESSING_FOUND to account_credit_types
Upgrade to 22.06.00.072  [21:41:50]: Bug 24381 - Update accounts notices
Upgrade to 22.06.00.073  [21:41:50]: Bug 30036 - Add XSLT for authority results view in OPAC
        Added new system preference 'AuthorityXSLTOpacResultsDisplay'
Upgrade to 22.06.00.074  [21:41:50]: Bug 30407 - Add ability to syspref UpdateNotForLoanStatusOnCheckin to show only the notforloan values message
Upgrade to 22.06.00.075  [21:41:50]: Bug 31948 - Add timestamp to tmp_holdsqueue table
Upgrade to 22.06.00.076  [21:41:50]: Bug 29792 - Fix transfers created from 'wrong transfer' checkin are not sent if modal dismissed
        Added new system preference 'AutomaticConfirmTransfer'
Upgrade to 22.06.00.077  [21:41:50]: Bug 31713 - Add ACCOUNTS_SUMMARY slip notice
        Added new letter 'ACCOUNTS_SUMMARY' (print)
Upgrade to 22.06.00.078  [21:41:50]: Bug 24860 - Add ability to place item group level holds
        Added new system preference 'EnableItemGroupHolds'
Upgrade to 22.06.00.079  [21:41:50]: Bug 32030 - Add an ERM module
        Added new system preference 'ERMModule'
        Added new permission 'erm'
        Added new table 'erm_agreements'
        Added new table 'erm_agreement_periods'
        Added new table 'erm_licenses'
        Added new table 'erm_agreement_licenses'
        Added new table 'erm_user_roles'
        Added new table 'erm_agreement_relationships'
        Added new table 'erm_documents'
        Added new table 'erm_eholdings_packages'
        Added new table 'erm_eholdings_packages_agreements'
        Added new table 'erm_eholdings_titles'
        Added new table 'erm_eholdings_resources'
        Added column 'aqbooksellers.external_id'
        Added new system preference 'ERMProviders'
        Added new system preference 'ERMProviderEbscoCustomerID'
        Added new system preference 'ERMProviderEbscoApiKey'
Upgrade to 22.06.00.080  [21:41:50]: Bug 30880 - Add branchonly option to OPACResultsUnavailableGroupingBy syspref
Upgrade to 22.06.00.081  [21:41:50]: Bug 31378 - Add identity_provider and identity_provider_domains configuration tables
        Added new permission 'manage_identity_providers'
        Added new table 'identity_providers'
        Added new table 'identity_provider_domains'
Upgrade to 22.06.00.082  [21:41:50]: Bug 30250 - Add new system preference ApplyFrameworkDefaults
        Added new system preference 'ApplyFrameworkDefaults'
Upgrade to 22.06.00.083  [21:41:50]: Bug 24606 - Add new table item_editor_templates
        Added new table 'item_editor_templates'
        Added new permission 'manage_item_editor_templates'
Upgrade to 22.06.00.084  [21:41:50]: Bug 32162 - Add primary key to erm_eholdings_packages_agreements
Upgrade to 22.06.00.085  [21:41:50]: Bug 32030 - Add primary key to erm_user_roles
Upgrade to 22.11.00.000  [21:41:50]: Koha 22.11.00 Rosalie release
Upgrade to 22.12.00.000  [21:41:50]: Increase DBRev for 22.12
        📜 Deep into that darkness peering, long I stood there wondering, fearing,
        📜 Doubting, dreaming dreams no mortal ever dared to dream before;
        📜 But the silence was unbroken, and the stillness gave no token
Upgrade to 22.12.00.001  [21:41:50]: Bug 32330 - Add indexes to background_jobs table
Upgrade to 22.12.00.002  [21:41:50]: Bug 27424 - Add column to specify an SMTP server as the default
Upgrade to 22.12.00.003  [21:41:50]: Bug 20256 - Add ability to limit editing of items to home library
        Added new permission 'edit_any_item'
        Added 'edit_any_item' permission to users with edit items permission
        Added column 'library_groups.ft_limit_item_editing'
Upgrade to 22.12.00.004  [21:41:50]: Bug 30642 - Record whether a renewal has been done manually or automatically.
        Added column 'checkout_renewals.column_name'
Upgrade to 22.12.00.005  [21:41:50]: Bug 31051 - Add new system preference OPACShowSavings
        Added new system preference 'OPACShowSavings'
Upgrade to 22.12.00.006  [21:41:50]: Bug 22428 - Changes the datatype of the field value column to text to stop input being cut short
        Amended dataype of column field_value in table marc_modification_template_actions.
Upgrade to 22.12.00.007  [21:41:50]: Bug 32967 - Recalls notices are using the wrong database columns
        Fix column names in PICKUP_RECALLED_ITEM notice
        Fix column names in RECALL_REQUESTER_DET notice
Upgrade to 22.12.00.008  [21:41:50]: Bug 33004 - Add VENDOR_TYPE authorised value category
        Added new authorised value category 'VENDOR_TYPE'
Upgrade to 22.12.00.009  [21:41:50]: Bug 32799 - Rename ILLSTATUS authorised value category
        Renamed authorised value category 'ILLSTATUS' to 'ILL_STATUS_ALIAS'
Upgrade to 22.12.00.010  [21:41:50]: Bug 31028 - Add a way to record users concerns about catalog records
        Added new table 'tickets'
        Added new table 'ticket_updates'
        Added new system preference 'OpacCatalogConcerns'
        `CatalogConcernHelp` block added to html_customization
        `CatalogConcernTemplate` block added to html_customization
        Added new notice 'TICKET_ACKNOWLEDGE'
        Added new notice 'TICKET_UPDATE'
        Added new notice 'TICKET_RESOLVE'
        Added new system preference 'CatalogerEmails'
        Added new notice 'TICKET_NOTIFY'
        Added new system preference 'CatalogConcerns'
Upgrade to 22.12.00.011  [21:41:50]: Bug 25655 - Store actual cost in foreign currency and currency from the invoices
        Added column 'aqorders.invoice_unitprice'
        Added column 'aqorders.invoice_currency'
Upgrade to 22.12.00.012  [21:41:50]: Bug 30624 - Add loggedinlibrary permission
        Added new permission 'loggedinlibrary'
Upgrade to 22.12.00.013  [21:41:50]: Bug 32057 - Add optional stack trace to action logs
        Added column 'action_logs.trace'
        Added new system preference 'ActionLogsTraceDepth'
Upgrade to 22.12.00.014  [21:41:50]: Bug 30555 - Add more sample notice for sms messages
        Added new letter 'CHECKIN' (sms)
        Added new letter 'CHECKOUT' (sms)
        Added new letter 'DUE' (sms)
        Added new letter 'DUEDGST' (sms)
        Added new letter 'PREDUE' (sms)
        Added new letter 'PREDUEDGST' (sms)
        Added new letter 'HOLD' (sms)
Upgrade to 22.12.00.015  [21:41:50]: Bug  3150 - Add LIST and CART notices
        Added new letter 'LIST' (email)
        Added new letter 'CART' (email)
Upgrade to 22.12.00.016  [21:41:50]: Bug 32437 - Add primary key to import_auths tables
        Added PRIMARY KEY ON import_record_id to import_authd table
Upgrade to 22.12.00.017  [21:41:50]: Bug 31123 - Add `ContentWarningField` preference
Upgrade to 22.12.00.018  [21:41:50]: Bug 30403 - Add system preference UpdateNotForLoanStatusOnCheckout
Upgrade to 22.12.00.019  [21:41:51]: Bug 33368 - Extend borrowers.flags to bigint
Upgrade to 22.12.00.020  [21:41:51]: Bug 33192 - Rename `AutoEmailPrimaryAddress` to `EmailFieldPrimary`
        Updated system preference 'AutoEmailPrimaryAddress'
Upgrade to 22.12.00.021  [21:41:51]: Bug 33103 - Add vendor aliases
        Added new table 'aqbookseller_aliases'
Upgrade to 22.12.00.022  [21:41:51]: Bug 12029 - Enable users to dismiss their patron messages
        Added column 'messages.patron_read_date'
Upgrade to 22.12.00.023  [21:41:51]: Bug 33300 - Fix missing wrong system preference 'AutomaticWrongTransfer'
        Wrong system preference 'AutomaticWrongTransfer' does not exist
Upgrade to 22.12.00.024  [21:41:51]: Bug 33128 - Add missing Polish (pl) language translations
        Polish (pl) translations were added
Upgrade to 22.12.00.025  [21:41:51]: Bug 32745 - Update context={} for invalid background jobs
Upgrade to 22.12.00.026  [21:41:51]: Bug 22440 - Add new /ill_requests endopoint
        Added column 'illrequests.deleted_biblio_id'
        Added foreign key constraint 'illrequests.illrequests_bibfk'
Upgrade to 22.12.00.027  [21:41:51]: Bug 33262 - Store biblionumber of deleted record in acquisition orders
        Added column 'aqorders.deleted_biblionumber'
Upgrade to 22.12.00.028  [21:41:51]: Bug 33104 - Add vendor interfaces
        Added new table 'aqbookseller_interfaces'
        Added new authorised value category 'VENDOR_INTERFACE_TYPE'
Upgrade to 22.12.00.029  [21:41:51]: Bug 33197 - Rename GDPR_Policy system preference
        Rename system preference GDPR_Policy to PrivacyPolicyConsent
Upgrade to 22.12.00.030  [21:41:51]: Bug 33053 - Remove default from biblio_id for item_groups and recalls tables
Upgrade to 22.12.00.031  [21:41:51]: Bug 33673 - Change "global system preferences" to "system preferences"
        Updated manage_sysprefs permission description.
Upgrade to 22.12.00.032  [21:41:51]: Bug 30928 - Add interface field to statistics table
        Added column 'statistics.interface'
Upgrade to 22.12.00.033  [21:41:52]: Bug 28328 - Extend biblioitems.lccn
Upgrade to 22.12.00.034  [21:41:52]: Bug 33557 - Add a system preference LinkerConsiderThesaurus
        Added new system preference 'LinkerConsiderThesaurus'
Upgrade to 22.12.00.035  [21:41:52]: Bug 33567 - Replace empty Reference_NFL_Statuses pref
Upgrade to 22.12.00.036  [21:41:52]: Bug 31557 - Add syspref HoldsQueuePrioritizeBranch
Upgrade to 22.12.00.037  [21:41:53]: Bug 31212 - Update items.datelastseen and deleteditems.datelastseen to datetime data format
        items and deleteditems table updated
Upgrade to 22.12.00.038  [21:41:53]: Bug 33489 - Add indices to default patron search fields
        Added new index on borrowers.cardnumber
        Added new index on borrowers.userid
        Added new index on borrowers.midddle_name
Upgrade to 22.12.00.039  [21:41:53]: Bug 32357 - Set borrower_message_preferences.days_in_advance default to NULL
        Updated column 'borrower_message_preferences.days_in_advance default' to NULL
Upgrade to 22.12.00.040  [21:41:53]: Bug 33488 - Add index to fromBranch for branch_transfer_limits
        Added new index on branch_transfer_limits.fromBranch
Upgrade to 22.12.00.041  [21:41:53]: Bug 30649 - Increase the vendor EDI account password field to 256 characters
Upgrade to 22.12.00.042  [21:41:53]: Bug 30418 - Add new list permission and new column to virtualshelves
Upgrade to 22.12.00.043  [21:41:53]: Bug 21330 - Add XSLT for authority details view in OPAC
        Added new system preference 'AuthorityXSLTOpacDetailsDisplay'
Upgrade to 22.12.00.044  [21:41:53]: Bug 11844 - Add column additional_fields.marcfield_mode
        Added column 'additional_fields.marcfield
Upgrade to 22.12.00.045  [21:41:53]: Bug 33297 - Fix missing 's' in system preference 'RetainPatronSearchTerms'
Upgrade to 22.12.00.046  [21:41:53]: Bug 30358 - Add new system preference StripWhitespaceChars
Upgrade to 22.12.00.047  [21:41:53]: Bug 32450 - Create a database flag for whether a debit type should be included in the noissuescharge block on circulation and remove redundant sysprefs.
        Added column 'account_debit_types.restricts_checkouts'
        ManInvInNoissuesCharge is included in the charge, default database value of 1 can be applied.
        RentalsInNoissuesCharge is included in the charge, default database value of 1 can be applied.
        HoldsInNoissuesCharge has been updated to not be included in the charge, account_debit_types has been updated to match this.
Upgrade to 22.12.00.048  [21:41:53]: Bug 29046 - Allow setting first_valid_email_address field precedence order
        Added new system preference 'EmailFieldPrecedence'
Upgrade to 23.05.00.000  [21:41:53]: Koha 23.05.00 release
Upgrade to 23.06.00.000  [21:41:53]: Increase DBRev for 23.06
        📜 Another one bites the dust;
        📜 and another one gone and another one gone.
        📜 Another one bites the dust.
        📜 Hey I'm gonna get you too!
        📜 Another one bites the dust.
Upgrade to 23.06.00.001  [21:41:53]: Bug 33697 - Remove RecordedBooks (rbdigital) integration
        Removed system preference 'RecordedBooksClientSecret'
        Removed system preference 'RecordedBooksDomain'
        Removed system preference 'RecordedBooksLibraryID'
Upgrade to 23.06.00.002  [21:41:53]: Bug 21983 - Deleted biblio handling on ILL
Upgrade to 23.06.00.003  [21:41:53]: Bug 32478 - Remove usage of Koha::Config::SysPref->find since bypasses cache
        Replace 'NULL' with 'null' in ItemsDeniedRenewal system preference
        Clear system preference cache
Upgrade to 23.06.00.004  [21:41:53]: Bug 33945 - Add system preference LoadCheckoutsTableDelay
Upgrade to 23.06.00.005  [21:41:53]: Bug 33961 - Remove Offline circulation tool
        Removed system preference 'AllowOfflineCirculation'
Upgrade to 23.06.00.006  [21:41:53]: Bug 33117 - Patron checkout is not able to find patrons if using a second surname or other name during the search
        Added new system preference 'DefaultPatronSearchMethod'
Upgrade to 23.06.00.007  [21:41:59]: Bug 34029 - Extend datatypes in biblioitems and deletedbiblioitems tables to avoid import errors
        Updated biblioitems.place to text
        Updated deletedbiblioitems.place to text
        Remove index on biblioitems.publishercode
        Updated biblioitems.publishercode to text
        Create index on biblioitems.publishercode
        Remove index on deletedbiblioitems.publishercode
        Updated deletedbiblioitems.publishercode to text
        Create index on deletedbiblioitems.publishercode
        Updated biblioitems.size to text
        Updated deletedbiblioitems.size to text
        Updated biblioitems.pages to text
        Updated deletedbiblioitems.pages to text
        Updated biblioitems.illus to text
        Updated deletedbiblioitems.illus to text
Upgrade to 23.06.00.008  [21:41:59]: Bug 33039 - Add published on template to serial subscriptions table
Upgrade to 23.06.00.009  [21:41:59]: Bug 30979 - Add OPACTrustedCheckout system preference
Upgrade to 23.06.00.010  [21:41:59]: Bug 33028 - Fix wrongly formatted values for monetary values in circulation rules
        Circulation rules have been validated. All circulation rule values are correctly formatted.
Upgrade to 23.06.00.011  [21:41:59]: Bug 33105 - Add vendor issues
        Added new table 'aqbookseller_issues'
        Added new permission 'acquisition.issue_manage'
        Added new authorised value category 'VENDOR_ISSUE_TYPE'
Upgrade to 23.06.00.012  [21:41:59]: Bug 33379 - Remove unused column virtualshelfcontents.flags
        Removed column 'virtualshelfcontents.flags'
Upgrade to 23.06.00.013  [21:41:59]: Bug 28966 - Holds queue view too slow to load for large numbers of holds
        Set primary key for table 'tmp_holdsqueue' to 'itemnumber'
Upgrade to 23.06.00.014  [21:41:59]: Bug 30451 - Update FK constraint on aqorders.subscriptionid to ON DELETE SET NULL
        Update FK constraint on subscriptionid
Upgrade to 23.06.00.015  [21:41:59]: Bug 34494 - Fix tmp_holdsqueue for MySQL compatibility
Upgrade to 23.06.00.016  [21:41:59]: Bug 34584 - Update SocialNetworks system preference to Choice
        Updated system preference 'SocialNetworks'
Upgrade to 23.06.00.017  [21:41:59]: Bug 32911 - Remove ILL partner_code config from koha-conf.xml and turn it into a system preference
Upgrade to 23.06.00.018  [21:41:59]: Bug 27378 - Adds the sysprefs for cookie consents
        Added new system preference 'CookieConsentedJS'
        Added new system preference 'CookieConsent'
Upgrade to 23.06.00.019  [21:41:59]: Bug 34789 - Correct datatypes and column name in table erm_eholdings_titles
        Column preceeding_publication_title renamed to preceding_publication_title_id
        Column publication_title datatype amended to mediumtext
        Column notes datatype amended to mediumtext
Upgrade to 23.06.00.020  [21:41:59]: Bug 27634 - Add categorycode and dateexpiry to PatronSelfRegistrationBorrowerUnwantedField
Upgrade to 23.06.00.021  [21:41:59]: Bug 33716 - Add new ILLModuleDisclaimerByType system preference
        Added new system preference 'ILLModuleDisclaimerByType'
Upgrade to 23.06.00.022  [21:41:59]: Bug 34844 - Add permission manage_item_editor_templates
        Added new permission 'manage_item_editor_templates'
Upgrade to 23.06.00.023  [21:41:59]: Bug 34843 - Restore comment on article_requests.toc_request
Upgrade to 23.06.00.024  [21:41:59]: Bug 34720 - Add system preference UpdateNotForLoanStatusOnCheckout
        Skipped - System preference exists already in DB
Upgrade to 23.06.00.025  [21:41:59]: Bug 29822 - Convert DefaultPatronSeachFields from csv to psv
        Updated system preference 'DefaultPatronSearchFields
Upgrade to 23.06.00.026  [21:41:59]: Bug 34748 - Fix column name in column configuration for basket summary
        Update column configuration with new columnname order_line
Upgrade to 23.06.00.027  [21:41:59]: Bug 29145 - Change type of AutoRemoveOverduesRestrictions system preference
        Type of AutoRemoveOverduesRestrictions system preference has been changed
Upgrade to 23.06.00.028  [21:41:59]: Bug  9525 - Add option to set group as local float group
        Added column 'library_groups.ft_local_float_group'
Upgrade to 23.06.00.029  [21:41:59]: Bug 34657 - Update MARC frameworks to use renamed UNIMARC plugin (unimarc_field_123defg.pl)
        Update complete: MARC subfields which were configured to use unimarc_field123d.pl, unimarc_field123e.pl, unimarc_field123f.pl, or unimarc_field123g.pl will now use unimarc_field123defg.pl
Upgrade to 23.06.00.030  [21:41:59]: Bug 28688 - Add notice MEMBERSHIP_RENEWED
Upgrade to 23.06.00.031  [21:41:59]: Bug 12532 - Add new system preference RedirectGuaranteeEmail and cc_address field
        Added system preference 'RedirectGuaranteeEmail'
        Added column 'cc_address'
Upgrade to 23.06.00.032  [21:41:59]: Bug 25560 - Migrating existing UpdateNotForLoanStatusOnCheckin rules to new format
Upgrade to 23.06.00.033  [21:41:59]: Bug 34075 - Add DefaultAuthorityTab system preference
        Added new system preference 'DefaultAuthorityTab'
Upgrade to 23.06.00.034  [21:41:59]: Bug 21246 - A preference to specify how many previous patrons to show for showLastPatron
        Added new system preference 'showLastPatronCount'
Upgrade to 23.06.00.035  [21:41:59]: Bug 16223 - Add new columns lift_after_payment and fee_limit to table restriction_types
        Added column 'restriction_types.lift_after_payment'
        Added column 'restriction_types.fee_limit'
Upgrade to 23.06.00.036  [21:41:59]: Bug 30719 - Add ability to create batch ILL requests
        Added new table 'illbatch_statuses'
        Added new table 'illbatches'
        Added column 'illrequests.batch_id'
        Added new ILL batch status 'NEW'
        Added new ILL batch status 'IN_PROGRESS'
        Added new ILL batch status 'COMPLETED'
        Added new ILL batch status 'UNKNOWN'
Upgrade to 23.06.00.037  [21:41:59]: Bug 31631 - Allow choosing for tax-exclusive values to be used for calculating fund values (spent, ordered)
        Added new system preference 'CalculateFundValuesIncludingTax'
Upgrade to 23.06.00.038  [21:41:59]: Bug 30708 - Add a preservation module
        Added new system preference 'PreservationModule'
        Added new system preference 'PreservationNotForLoanWaitingListIn'
        Added new system preference 'PreservationNotForLoanDefaultTrainIn'
        Added new permission 'preservation'
        Added new table 'preservation_processings'
        Added new table 'preservation_trains'
        Added new table 'preservation_processing_attributes'
        Added new table 'preservation_trains_items'
        Added new table 'preservation_processing_attributes_items'
Upgrade to 23.06.00.039  [21:41:59]: Bug 32721 - Allow branch specific javascript and css to be injected into the OPAC depending on a branchcode
        Added column 'branches.opacuserjs'
        Added column 'branches.opacusercss'
Upgrade to 23.06.00.040  [21:41:59]: Bug 25816 - Add OPAC messages in SIP display
        Added new system preference 'SIP2AddOpacMessagesToScreenMessage'
Upgrade to 23.06.00.041  [21:41:59]: Bug 31383 - Split the additional_contents table
        Renamed additional_contents.idnew with 'id'
        Added new table 'additional_contents_localizations'
        Removed 'title', 'content', 'lang' columns from additional_contents
Upgrade to 23.06.00.042  [21:41:59]: Bug 33845 - Update holds_table column settings entries to holds-table
        Update columns settings to use table name holds-table
Upgrade to 23.06.00.043  [21:41:59]: Bug 31357 - Add new system preference IntranetReadingHistoryHolds
Upgrade to 23.06.00.044  [21:41:59]: Bug 25393 - Create separate 'no automatic renewal before' rule
        New circulation rule 'noautorenewalbefore' has been added. Defaulting value to 'norenewalbefore'.
Upgrade to 23.06.00.045  [21:41:59]: Bug 28166 - Add system preference for additional columns for Z39.50 authority search results
        Added new system preference 'AdditionalFieldsInZ3950ResultAuthSearch'
Upgrade to 23.06.00.046  [21:41:59]: Bug 33547 - Add a new notice template 'PRES_TRAIN_ITEM'
        Added new letter 'PRES_TRAIN_ITEM' (print)
Upgrade to 23.06.00.047  [21:41:59]: Bug 15504 - Adds a new system preference - TrackLastPatronActivityTriggers
        Added system preference 'TrackLastPatronActivityTriggers'
        Removed system preference 'TrackLastPatronActivity'
Upgrade to 23.06.00.048  [21:41:59]: Bug 27153 - Add option to filter search fields
        Added column 'search_marc_to_field.filter'
        Updated primary key to include filter
Upgrade to 23.06.00.049  [21:41:59]: Bug 31503 - Change patron_consent.type
        Changed column 'patron_consent.type'
Upgrade to 23.06.00.050  [21:41:59]: Bug 31846 - Allow setting serials search results limit
        Added new system preference 'SerialsSearchResultsLimit'
Upgrade to 23.06.00.051  [21:42:00]: Bug 10762 - Make it possible to adjust the barcode height and width on labels
        Added column 'creator_layouts.scale_width'
        Added column 'creator_layouts.scale_height'
Upgrade to 23.06.00.052  [21:42:00]: Bug  8838 - Add digest option for HOLD notice
        Added new notice 'HOLDDGST' (email)
        Added new notice 'HOLDDGST' (sms)
Upgrade to 23.06.00.053  [21:42:00]: Bug 33970 - Bind ILL attributes to specific backends
        Added column 'illrequestattributes.backend'
        ERROR: {UNKNOWN}: DBI Exception: DBD::mysql::db do failed: Can't DROP FOREIGN KEY `illrequestattributes_ifk`; check that it exists at /usr/share/koha/lib/C4/Installer.pm line 743
```

# Version 23.0600052 to 24.0600023

```
Upgrade to 23.06.00.053  [21:45:17]: Bug 33970 - Bind ILL attributes to specific backends
Upgrade to 23.06.00.054  [21:45:17]: Bug 33887 - Automatically fill the next hold with a automatic check in.
        Added new system preference 'AutomaticCheckinAutoFill'
Upgrade to 23.06.00.055  [21:45:17]: Bug 34520 - Correct item_groups FK in reserves table
        FK 'reserves_ibfk_ig' on reserves updated to ON DELETE SET NULL
Upgrade to 23.06.00.056  [21:45:17]: Bug 34587 - Add ERM Usage Statistics module
        Added new table 'erm_usage_data_providers'
        Added new table 'erm_counter_files'
        Added new table 'erm_counter_logs'
        Added new table 'erm_usage_titles'
        Added new table 'erm_usage_platforms'
        Added new table 'erm_usage_databases'
        Added new table 'erm_usage_items'
        Added new table 'erm_usage_mus'
        Added new table 'erm_usage_yus'
        Added new table 'erm_default_usage_reports'
Upgrade to 23.06.00.057  [21:45:17]: Bug 26170 - Add protected status for patrons
        Added column 'borrowers.protected'
        Added column 'deletedborrowers.protected'
Upgrade to 23.06.00.058  [21:45:17]: Bug 33664 - Allow cancelling of orders from closed baskets
        Added new system preference 'CancelOrdersInClosedBaskets'
Upgrade to 23.06.00.059  [21:45:17]: Bug  8367 - Set hold pickup period circulation rule
        Added default circulation rule for holds_pickup_period
Upgrade to 23.06.00.060  [21:45:17]: Bug 18203 - Add per borrower category restrictions on ILL placement
        Added column 'categories.can_place_ill_in_opac'
Upgrade to 23.06.00.061  [21:45:17]: Bug 29002 - Add bookings table
        Added new table 'bookings'
        Added column 'items.bookable'
        Added column 'deleteditems.bookable'
        Added new permission 'manage_bookings'
Upgrade to 23.06.00.062  [21:45:17]: Bug 35190 - Allow null values for authorized_value_category in additional_fields
        Altered authorized_value_category in additional_fields to set NULL as the default value
Upgrade to 23.06.00.063  [21:45:17]: Bug 21159 - Add new system preference UpdateItemLocationOnCheckout
        Added new system preference 'UpdateItemLocationOnCheckout'
Upgrade to 23.06.00.064  [21:45:17]: Bug 34557 - Add system preference SCOLoadCheckoutsByDefault
        Added new system preference 'SCOLoadCheckoutsByDefault'
Upgrade to 23.06.00.065  [21:45:17]: Bug 34438 - Add lang to to the borrower_modifications table
Upgrade to 23.06.00.066  [21:45:17]: Bug 20755 - Add sysprefs for email addresses in acquisitions and serials
        Added new system preference 'AcquisitionsDefaultEMailAddress'
        Added new system preference 'AcquisitionsDefaultReplyTo'
        Added new system preference 'SerialsDefaultEMailAddress'
        Added new system preference 'SerialsDefaultReplyTo'
Upgrade to 23.06.00.067  [21:45:17]: Bug 17617 - Notify patron when their hold has been placed
        Added new system preference 'EmailPatronWhenHoldIsPlaced'
        Added new letter 'HOLDPLACED_PATRON' (email)
Upgrade to 23.06.00.068  [21:45:17]: Bug 23798 - Convert OpacMaintenanceNotice system preference to additional contents
        Removed system preference 'OpacMaintenanceNotice'
Upgrade to 23.06.00.069  [21:45:17]: Bug 34869 - Move OPACResultsSidebar to additional contents
        Removed system preference 'OPACResultsSidebar'
Upgrade to 23.06.00.070  [21:45:17]: Bug 34889 - Move PatronSelfRegistrationAdditionalInstructions to additional contents
        Removed system preference 'PatronSelfRegistrationAdditionalInstructions'
Upgrade to 23.06.00.071  [21:45:17]: Bug 34328 - Add Scottish Gaelic to recognised languages
        Added new language 'Scottish Gaelic'
Upgrade to 23.06.00.072  [21:45:17]: Bug 34188 - Force staff to select a library when logging into the staff interface.
        Added new system preference 'ForceLibrarySelection'
Upgrade to 23.06.00.073  [21:45:17]: Bug 33217 - Add option to specify sorting for author links
        Added new system preferences 'AuthorLinkSortBy' and 'AuthorLinkSortOrder'
Upgrade to 23.06.00.074  [21:45:17]: Bug 34894 - Move OpacSuppressionMessage to additional contents
        Removed system preference 'OpacSuppressionMessage'
Upgrade to 23.06.00.075  [21:45:17]: Bug 34517 - Add option to specify which patron attributes are searched by default
        Added column 'borrower_attribute_types.searched_by_default'
        Updated values to match staff_searchable columns
Upgrade to 23.06.00.076  [21:45:17]: Bug 35048 - Move SCOMainUserBlock to additional contents
        Removed system preference 'SCOMainUserBlock'
Upgrade to 23.06.00.077  [21:45:17]: Bug 35063 - Move SelfCheckInMainUserBlock to additional contents
        Removed system preference 'SelfCheckInMainUserBlock'
Upgrade to 23.06.00.078  [21:45:17]: Bug 35065 - Move SelfCheckHelpMessage to additional contents
        Removed system preference 'SelfCheckHelpMessage'
Upgrade to 23.06.00.079  [21:45:17]: Bug 12133 - Add system preference ChildNeedsGuarantor
        Added new system preference 'ChildNeedsGuarantor'
Upgrade to 23.11.00.000  [21:45:17]: Koha 23.11.00 release
Upgrade to 23.12.00.000  [21:45:17]: Increase DBRev for 23.12
        📜 Bugs will happen. (Nick Clemens)
        📜 It's all about the people. (Chris Cormack)
Upgrade to 23.12.00.001  [21:45:17]: Bug 35413 - Terminology: Manage issues (issue_manage)
        Updated permission 'issue_manage' description with 'Manage vendor issues'
Upgrade to 23.12.00.002  [21:45:17]: Bug 31297 - Allow subscription number pattern description to be NULL
        Modified column 'subscription_numberpatterns.description' to allow and default to NULL
Upgrade to 23.12.00.003  [21:45:17]: Bug 26831 - Add new system preference PurgeListShareInvitesOlderThan
Upgrade to 23.12.00.004  [21:45:17]: Bug 35687 - Upgrade to 23.06.00.013 may fail, drop FK and recreate after adding the PK to tmp_holdsqueue
        Set primary key for table 'tmp_holdsqueue' to 'itemnumber'
Upgrade to 23.12.00.005  [21:45:17]: Bug 34979 - Fix system preference discrepancies
        Fix mistakes in system preferences, if necessary:
        Updated system preferences: OAI-PMH:AutoUpdateSetsEmbedItemData, OPACPrivacy
Upgrade to 23.12.00.006  [21:45:17]: Bug 30230 - Add new list_borrowers permission
        Added new permission 'list_borrowers'
Upgrade to 23.12.00.007  [21:45:17]: Bug 35872 - Biblio.HoldsCount is deprecated
Upgrade to 23.12.00.008  [21:45:17]: Bug 27595 - Add system preference PlaceHoldsOnOrdersFromSuggestions
        Added new system preference 'PlaceHoldsOnOrdersFromSuggestions'
Upgrade to 23.12.00.009  [21:45:17]: Bug 34668 - Notify staff with a pop-up about waiting holds when checking out
        Added new system preference 'WaitingNotifyAtCheckout'
Upgrade to 23.12.00.010  [21:45:17]: Bug 36033 - Add more indexes to pseudonymized_transactions
        Added new index on pseudonymized_transactions.itemnumber
        Added new index on pseudonymized_transactions.transaction_type
        Added new index on pseudonymized_transactions.datetime
Upgrade to 23.12.00.011  [21:45:17]: Bug 35873 - Biblio.RecallsCount is deprecated
Upgrade to 23.12.00.012  [21:45:17]: Bug 35386 - Add RESTAPIRenewalBranch preference
        Added new system preference 'RESTAPIRenewalBranch'
Upgrade to 23.12.00.013  [21:45:17]: Bug 23208 - Add system preference HoldRatioDefault
        Added new system preference 'HoldRatioDefault'
Upgrade to 23.12.00.014  [21:45:17]: Bug 36244 - Template Toolkit syntax not escaped in letter templates
Upgrade to 23.12.00.015  [21:45:17]: Bug 35610 - Add FK on old_reserves.branchcode
        Added foreign key on 'old_reserves.branchcode'
Upgrade to 23.12.00.016  [21:45:17]: Bug 36409 - Fix capitalization for SerialsDefaultEMailAddress and AcquisitionsDefaultEMailAddress
        Updated system preference 'SerialsDefaultEMailAddress' -> 'SerialsDefaultEmailAddress'
        Updated system preference 'AcquisitionsDefaultEMailAddress' -> 'AcquisitionsDefaultEmailAddress'
Upgrade to 23.12.00.017  [21:45:17]: Bug 32707 - Add 'ESPreventAutoTruncate' system preference
        Added new system preference 'ESPreventAutoTruncate'
Upgrade to 23.12.00.018  [21:45:17]: Bug  6796 - Overnight checkouts taking into account opening and closing hours
        Added table 'library_hours'
        Added system preference 'ConsiderLibraryHoursInCirculation'
Upgrade to 23.12.00.019  [21:45:17]: Bug 36051 - Add option to specify SMS::Send driver parameters in a system preference instead of a file
        Added new system preference 'SMSSendAdditionalOptions'
Upgrade to 23.12.00.020  [21:45:17]: Bug 36343 - Update plugin hooks for consistency
        WARNING: Plugin authors should consider changes introduced here
        WARNING: after_biblio_action, after_item_action and patron_generate_userid hooks now pass data inside a 'payload' hash
Upgrade to 23.12.00.021  [21:45:17]: Bug 35973 - Correct system preference 'RedirectGuaranteeEmail'
        Corrected system preference 'RedirectGuaranteeEmail'
Upgrade to 23.12.00.022  [21:45:17]: Bug 35724 - Add new fields to EDI accounts for librarians to configure non-standard EDI SFTP port numbers
        Added column 'vendor_edi_accounts.download_port'
        Added column 'vendor_edi_accounts.upload_port'
Upgrade to 23.12.00.023  [21:45:17]: Bug 32132 - Set aqbudgets.budget_period_id as NOT NULL
        Dropped foreign key aqbudgetperiods_ibfk_1
        Updated aqbudgets.budget_period_id to NOT accept NULL values
        Readded foreign key aqbudgetperiods_ibfk_1
Upgrade to 23.12.00.024  [21:45:17]: Bug 35065 - Move ILLModuleCopyrightClearance to additional contents
        Removed system preference 'ILLModuleCopyrightClearance'
Upgrade to 23.12.00.025  [21:45:17]: Bug 33393 - Modify sentence above the order table in English 1-page order PDF
        Added system preference '1PageOrderPDFText'
Upgrade to 23.12.00.026  [21:45:17]: Bug 35616 - Add source column to tickets table
        Added column 'tickets.source'
Upgrade to 23.12.00.027  [21:45:17]: Bug 32602 - Add administrative plugins type
        Added new permission 'plugins_admin'
Upgrade to 23.12.00.028  [21:45:17]: Bug 16122 - Add localuse column to items table and deleted items table
        Added column 'items.localuse'
        Added column 'deleteditems.localuse'
        You may use the new /misc/maintenance/update_localuse_from_statistics.pl script to populate the new field from the existing statistics data
Upgrade to 23.12.00.029  [21:45:19]: Bug 35919 - Add record_sources table
        Added new table 'record_sources'
        Added new column 'biblio_metadata.record_source_id'
        Added new foreign key 'biblio_metadata.record_metadata_fk_2'
        Added new column 'deletedbiblio_metadata.record_source_id'
        Added new foreign key 'deletedbiblio_metadata.record_metadata_fk_2'
        Added new permission 'manage_record_sources'
Upgrade to 23.12.00.030  [21:45:19]: Bug 35728 - Add option to NOT redirect to result when search returns only one record
        Added system preference 'RedirectToSoleResult'
Upgrade to 23.12.00.031  [21:45:19]: Bug 31791 - Add the ability to lock record modification
        Added new permission 'editcatalogue.edit_locked_records'
        Added new permission 'editcatalogue.set_record_sources'
Upgrade to 23.12.00.032  [21:45:19]: Bug 33478 - Customise the format of notices when they are printed
        Added column 'letter.style'
Upgrade to 23.12.00.033  [21:45:19]: Bug 31652 - Add geo-search: new value for search_field.type enum
        Added new value 'geo_point' to search_field.type enum
Upgrade to 23.12.00.034  [21:45:19]: Bug 12802 - Change type of system preference EmailFieldPrimary to multiple
        Updated system preference 'EmailFieldPrimary' to include 'selected addresses' option
        Added new system preference 'EmailFieldSelection'
Upgrade to 23.12.00.035  [21:45:19]: Bug 29393 - Add permission borrowers:send_messages_to_borrowers
        Added new permission 'send_messages_to_borrowers'
Upgrade to 23.12.00.036  [21:45:19]: Bug 35138 - Make the Elasticsearch facets configurable
        Updated DisplayLibraryFacets and search field configuration
Upgrade to 23.12.00.037  [21:45:19]: Bug 35626 - Add statuses to catalog concerns
        Added column 'tickets.status'
        Added column 'ticket_updates.status'
        Added TICKET_STATUS authorised value category
Upgrade to 23.12.00.038  [21:45:19]: Bug 32435 - Add ticket resolutions to catalog concerns
        Added TICKET_RESOLUTION authorised value category
Upgrade to 23.12.00.039  [21:45:19]: Bug 36002 - Remove aqorders.purchaseordernumber
Upgrade to 23.12.00.040  [21:45:19]: Bug 32610 - Add option for additional patron attributes of type date
        Added column 'borrower_attribute_types.is_date'
Upgrade to 23.12.00.041  [21:45:19]: Bug 15565 - Add DisplayMultiItemHolds system preference
        Added new system preference 'DisplayMultiItemHolds'
Upgrade to 23.12.00.042  [21:45:20]: Bug 35657 - Add assignee_id to tickets
        Added column 'tickets.assignee_id'
        Added column 'ticket_updates.assignee_id'
Upgrade to 23.12.00.043  [21:45:20]: Bug 25159 - Add action logs should be stored in JSON ( and as a diff of the change )
        Added column 'action_logs.diff'
Upgrade to 23.12.00.044  [21:45:20]: Bug 36120 - Add pickup location to bookings
        No bookings found that need updating to include a pickup library
Upgrade to 23.12.00.045  [21:45:20]: Bug 22740 - Preferences to enable automated setting of lost status when the associated fine is paid or written off
        Added new system preference 'UpdateItemLostStatusWhenPaid'
        Added new system preference 'UpdateItemLostStatusWhenWriteoff'
Upgrade to 23.12.00.046  [21:45:20]: Bug 27753 - Automate resolution of return claim when checking in an item
        Added new system preference 'AutoClaimReturnStatusOnCheckin'
        Added new system preference 'AutoClaimReturnStatusOnCheckout'
Upgrade to 23.12.00.047  [21:45:20]: Bug 35169 - Add new system preferences for longoverdue.pl borrowers categories
        Added new system preference 'DefaultLongOverduePatronCategories'
        Added new system preference 'DefaultLongOverdueSkipPatronCategories'
Upgrade to 23.12.00.048  [21:45:20]: Bug 33134 - Add some 76 missing languages
        Added 76 new languages
Upgrade to 23.12.00.049  [21:45:20]: Bug 36396 - Link Elasticsearch facets with authorized value categories
        Added Elasticsearch facets with authorized value categories
Upgrade to 23.12.00.050  [21:45:20]: Bug 36687 - Set itemtypes.notforloan to NOT NULL and tinyint(1)
        Updated itemtypes.notforlaon column'
Upgrade to 23.12.00.051  [21:45:20]: Bug 31097 - Change default 'Manual' restriction test
        Updated patron restriction types display for MANUAL restrictions from 'Manual' to 'Manual restriction'
Upgrade to 23.12.00.052  [21:45:20]: Bug 32256 - Self checkout batch mode
        Added system preference 'SCOBatchCheckoutsValidCategories'
Upgrade to 23.12.00.053  [21:45:20]: Bug 36755 - Increase length of 'code' column in borrower_attribute_types
        Increased borrower_attribute_types.code column length from 10 to 64
Upgrade to 23.12.00.054  [21:45:20]: Bug 19768 - Add 'Title notes' tab to OpacSerialDefaultTab system preference
        Added 'Title notes' option to opacSerialDefaultTab system preference
Upgrade to 23.12.00.055  [21:45:20]: Bug 30047 - Add thesaurus and heading fields to auth_header table
        Added column 'auth_header.heading'
Upgrade to 23.12.00.056  [21:45:20]: Bug 35149 - Add 'do nothing' option to CircAutoPrintQuickSlip syspref explanation
        Updated system preference 'CircAutoPrintQuickSlip'
Upgrade to 23.12.00.057  [21:45:20]: Bug 29948 - Display author information for researchers
        Added new system preference 'OPACAuthorIdentifiersAndInformation'
          Removed system preference 'OPACAuthorIdentifiers'
Upgrade to 23.12.00.058  [21:45:20]: Bug 28869 - Add authorised_value_categories.is_integer_only
Upgrade to 23.12.00.059  [21:45:20]: Bug 36819 - Change barcode width value if it still has the wrong default value
        Changed the barcode width in patron card creator default layout from 8% to 80%.
Upgrade to 23.12.00.060  [21:45:20]: Bug 36665 - Add system preference StaffLoginBranchBasedOnIP
        Added new system preference 'StaffLoginBranchBasedOnIP'
Upgrade to 23.12.00.061  [21:45:20]: Bug 26176 - Rename AutoLocation and StaffLoginBranchBasedOnIP system preferences
        Renamed system preference 'AutoLocation' to 'StaffLoginRestrictLibraryByIP'
        Renamed system preference 'StaffLoginBranchBasedOnIP' to 'StaffLoginLibraryBasedOnIP'
Upgrade to 24.05.00.000  [21:45:20]: Koha 24.05.00 release
Upgrade to 24.06.00.000  [21:45:20]: Increase DBRev for 24.06
        🎵 Mamma mia, here we go again!
Upgrade to 24.06.00.001  [21:45:20]: Bug 36986 - Rename StaffLoginLibraryBasedOnIP system preference
Upgrade to 24.06.00.002  [21:45:20]: Bug 36453 - BlockExpiredPatronOpacActions should allow multiple actions options
        BlockExpiredPatronOpacActions system preference type updated to multiple.
        BlockExpiredPatronOpacActions system preference value updated to an empty string.
        Updated categories.BlockExpiredPatronOpacActions to varchar(128)
        Patron categories BlockExpiredPatronOpacActions = -1 have been updated to follow the syspref BlockExpiredPatronOpacActions.
Upgrade to 24.06.00.003  [21:45:20]: Bug 34597 - Update BlockExpiredPatronOpacActions to include ill_request
        BlockExpiredPatronOpacActions system updated to include ill_request.
Upgrade to 24.06.00.004  [21:45:20]: Bug 18493 - Add missing languages to search options
        Added language_subtag_registry for Greenlandic
        Added language_rfc4646_to_iso639 for Greenlandic
        Added english language description for Greenlandic
        Added native language description for Greenlandic
        Added language_subtag_registry for Karelian
        Added language_rfc4646_to_iso639 for Karelian
        Added english language description for Karelian
        Added native language description for Karelian
        Added language_subtag_registry for Cornish
        Added language_rfc4646_to_iso639 for Cornish
        Added english language description for Cornish
        Added native language description for Cornish
        Added language_subtag_registry for Burmese
        Added language_rfc4646_to_iso639 for Burmese
        Added english language description for Burmese
        Added native language description for Burmese
        Added language_subtag_registry for Punjabi
        Added language_rfc4646_to_iso639 for Punjabi
        Added english language description for Punjabi
        Added native language description for Punjabi
        Added language_subtag_registry for Pashto
        Added language_rfc4646_to_iso639 for Pashto
        Added english language description for Pashto
        Added native language description for Pashto
        Added language_rfc4646_to_iso639 for Finnish Kalo
        Added english language description for Finnish Kalo
        Added native language description for Finnish Kalo
        Added native language description for Finnish Kalo
        Added language_subtag_registry for Akkala Sami
        Added language_rfc4646_to_iso639 for Akkala Sami
        Added english language description for Akkala Sami
        Added native language description for Akkala Sami
        Added language_subtag_registry for Kildin Sami
        Added language_rfc4646_to_iso639 for Kildin Sami
        Added english language description for Kildin Sami
        Added native language description for Kildin Sami
        Added language_subtag_registry for Ter Sami
        Added language_rfc4646_to_iso639 for Ter Sami
        Added english language description for Ter Sami
        Added native language description for Ter Sami
        Added language_subtag_registry for Pite Sami
        Added language_rfc4646_to_iso639 for Pite Sami
        Added english language description for Pite Sami
        Added native language description for Pite Sami
        Added language_subtag_registry for Kemi Sami
        Added language_rfc4646_to_iso639 for Kemi Sami
        Added english language description for Kemi Sami
        Added native language description for Kemi Sami
        Added language_subtag_registry for Ume Sami
        Added language_rfc4646_to_iso639 for Ume Sami
        Added english language description for Ume Sami
        Added native language description for Ume Sami
        Added language_subtag_registry for Southern Sami
        Added language_rfc4646_to_iso639 for Southern Sami
        Added english language description for Southern Sami
        Added native language description for Southern Sami
        Added language_subtag_registry for Northern Sami
        Added language_rfc4646_to_iso639 for Northern Sami
        Added english language description for Northern Sami
        Added native language description for Northern Sami
        Added native language description for Northern Sami
        Added native language description for Northern Sami
        Added language_subtag_registry for Sami languages
        Added language_rfc4646_to_iso639 for Sami languages
        Added english language description for Sami languages
        Added native language description for Sami languages
        Added native language description for Sami languages
        Added native language description for Sami languages
        Added language_subtag_registry for Lule Sami
        Added language_rfc4646_to_iso639 for Lule Sami
        Added english language description for Lule Sami
        Added native language description for Lule Sami
        Added language_subtag_registry for Inari Sami
        Added language_rfc4646_to_iso639 for Inari Sami
        Added english language description for Inari Sami
        Added native language description for Inari Sami
        Added language_subtag_registry for Skolt Sami
        Added language_rfc4646_to_iso639 for Skolt Sami
        Added english language description for Skolt Sami
        Added native language description for Skolt Sami
        Added language_subtag_registry for Somali
        Added language_rfc4646_to_iso639 for Somali
        Added english language description for Somali
        Added native language description for Somali
        Added language_subtag_registry for Sotho
        Added language_rfc4646_to_iso639 for Sotho
        Added english language description for Sotho
        Added native language description for Sotho
        Added language_subtag_registry for Votic
        Added language_rfc4646_to_iso639 for Votic
        Added english language description for Votic
        Added native language description for Votic
        Updated native lv language description from Latvija to Latviešu valoda
        Updated native lt language description from Lietuvių to Lietuvių kalba
        Added native language description for Ancient Greek
        Added native language description for Esperanto
        Added native language description for Sanskrit
        Added native language description for Irish Gaelic
        Added native language description for Bosnian
        Added native language description for Kazakh
        Added native language description of Standard Tibetan
        Added native language description of Welsh
Upgrade to 24.06.00.005  [21:45:20]: Bug 35639 - Add the SMSSendMaxChar system preference to limit the number of characters in a SMS message
        Added new system preference 'SMSSendMaxChar'
Upgrade to 24.06.00.006  [21:45:20]: Bug 35597 - Add SuggestionsLog system preference
        Added new system preference 'SuggestionsLog'
Upgrade to 24.06.00.007  [21:45:20]: Bug 36330 - Fix typo 'reseve' in COMMENTs for table  course_items
        Comment for course_items.location was updated.
        Comment for course_items.enabled was updated.
Upgrade to 24.06.00.008  [21:45:20]: Bug 35153 - Move IntranetmainUserblock to additional contents
        Removed system preference 'IntranetmainUserblock'
Upgrade to 24.06.00.009  [21:45:20]: Bug 33317 - Add new system preference OpacMetaRobots
        Added system preference 'OpacMetaRobots'
Upgrade to 24.06.00.010  [21:45:20]: Bug 34481 - Add IncludeSeeAlsoFromInSearches like IncludeSeeFromInSearches
        Added new system preference 'IncludeSeeAlsoFromInSearches'
Upgrade to 24.06.00.011  [21:45:20]: Bug 37216 - Ensure EmailFieldSelection options are correct
        Updated system preference 'EmailFieldSelection'
Upgrade to 24.06.00.012  [21:45:20]: Bug 26205 - Add new system preference OPACShowLibraries
        Added new system preference 'OPACShowLibraries'
Upgrade to 24.06.00.013  [21:45:20]: Bug 18317 - Allow check out of already checked out items through SIP
        Added new system preference 'AllowItemsOnLoanCheckoutSIP'
Upgrade to 24.06.00.014  [21:45:20]: Bug 33363 - Split suggestions_manage into three separate permissions for creating, updating, and deleting suggetions
        Added new permissions suggestions_create
        Added new permissions suggestions_delete
        Added new permissions suggestions_create to patrons with suggestions_manage
        Added new permissions suggestions_delete to patrons with suggestions_manage
Upgrade to 24.06.00.015  [21:45:20]: Bug 36453 - Update BlockExpiredPatronOpacActions where 24.06.000.02 was already run
        categories.BlockExpiredPatronOpacActions already varchar(128)
Upgrade to 24.06.00.016  [21:45:20]: Bug 28924 - Adds columns to patron categories to allow category level values for the no issue charge sysprefs
        Added column 'noissuescharge' to categories
        Added column 'noissueschargeguarantees' to categories
        Added column 'noissueschargeguarantorswithguarantees' to categories
Upgrade to 24.06.00.017  [21:45:20]: Bug 13888 - 'Lists' permission should allow/disallow using the lists module in staff
        Added permission 'use_public_lists'
        Added permission 'create_public_lists'
Upgrade to 24.06.00.018  [21:45:20]: Bug 29509 - Update users with list_borrowers permission where required
        list_borrowers added to 4 users with manage_bookings
        list_borrowers added to 7 users with label_creator
        list_borrowers added to 3 users with routing
        list_borrowers added to 3 users with order_manage
Upgrade to 24.06.00.019  [21:45:20]: Bug 23781 - Recalls notices and messaging preferences
        Added recalls SMS notices: RETURN_RECALLED_ITEM, PICKUP_RECALLED_ITEM
        Added message attributes for recalls: Recall_Waiting, Recall_Requested
        Added message transports for recalls notices
Upgrade to 24.06.00.020  [21:45:20]: Bug 36996 - Add z3950Status system preference
        Added new system preference 'Z3950Status'
Upgrade to 24.06.00.021  [21:45:20]: Bug 35539 - Remove unused columns from 'categories' table
        Removed 'bulk' column from 'categories' table
        Removed 'finetype' column from 'categories' table
        Removed 'issuelimit' column from 'categories' table
Upgrade to 24.06.00.022  [21:45:22]: Bug 37419 - Replace FK constraint to avoid data loss
        Updated foreign key 'biblio_metadata.record_metadata_fk_2'
Upgrade to 24.06.00.023  [21:45:22]: Bug 36757 - Notify assignee when a concern is assigned to them
        Added notice 'TICKET_ASSIGNED'
Upgrade to 24.06.00.024  [21:45:22]: Bug 35044 - Add repeatable option to additional_fields
        Added repeatable column to additional_fields table
        ERROR: {UNKNOWN}: DBI Exception: DBD::mysql::db do failed: Can't DROP FOREIGN KEY `afv_fk`; check that it exists at /usr/share/koha/lib/C4/Installer.pm line 743
```

## Version 24.0600023 to 24.1102000 (Latest)

```
0E0
Upgrade to 24.06.00.025  [22:02:26]: Bug 26777 - Adds new system preferences 'OPACVirtualCard and 'OPACVirtualCardBarcode'
        Added new system preference 'OPACVirtualCard'
        Added new system preference 'OPACVirtualCardBarcode'
Upgrade to 24.06.00.026  [22:02:26]: Bug 20411 - Remove StaffDetailItemSelection system preference
        Removed system preference 'StaffDetailItemSelection'
Upgrade to 24.06.00.027  [22:02:26]: Bug 27490 - Change language syspref to StaffInterfaceLanguages
        Updated system preference 'language' to 'StaffInterfaceLanguages'
Upgrade to 24.06.00.028  [22:02:26]: Bug 37757 - More robust handling of EmailFieldPrimary system preference values
        Updated system preference 'EmailFieldPrimary'
Upgrade to 24.06.00.029  [22:02:26]: Bug 37592 - Add creation_date, modification_date fields to bookings table
        Added column 'bookings.creation_date'
        Added column 'bookings.modification_date'
Upgrade to 24.06.00.030  [22:02:26]: Bug 37601 - Add status column to bookings table
        Added column 'bookings.status'
Upgrade to 24.06.00.031  [22:02:26]: Bug 23685 - Add system preferences ReportsExportFormatODS and ReportsExportLimit
        Added new system preferences 'ReportsExportFormatODS' and 'ReportsExportLimit'
Upgrade to 24.06.00.032  [22:02:26]: Bug 37856 - Add column 'erm_usage_data_providers.service_platform'
        Added column 'service_platformerm_usage_data_providers'
Upgrade to 24.06.00.033  [22:02:26]: Bug 35655 - Add a way to disable RabbitMQ
        Added new system preference 'JobsNotificationMethod'
Upgrade to 24.06.00.034  [22:02:26]: Bug 37967 - Add auto renewal message_transport for phone
        Added phone messaging transports for auto-renewals
Upgrade to 24.06.00.035  [22:02:26]: Bug 37446 - Fix holdingbranch and homebranch facet labels
        Updated search field configuration for holdingbranch and homebranch
Upgrade to 24.06.00.036  [22:02:26]: Bug 37954 - Move holdings_barcodes setting to holdings_barcode
        No settings for holdings_barcodes found
        Removed settings for holdings_barcodes
Upgrade to 24.06.00.037  [22:02:26]: Bug 36798 - Add 'SearchCancelledAndInvalidISBNandISSN' preference
        Added new system preference 'SearchCancelledAndInvalidISBNandISSN'
Upgrade to 24.06.00.038  [22:02:26]: Bug 36766 - Add command-line utility to SFTP a file to a remote server
        Added new sample notices 'SFTP_FAILURE' and 'SFTP_SUCCESS'
Upgrade to 24.06.00.039  [22:02:26]: Bug 28575 - Add a system preference to prevent refunds on lost items if the fee was paid more than a set number of days ago
        Added new system preference 'NoRefundOnLostFinesPaidAge'
Upgrade to 24.06.00.040  [22:02:26]: Bug 23295 - Automatically debar patrons if SMS or email notice fail
        Added new system preference 'RestrictPatronsWithFailedNotices'
        Added new system restriction type 'NOTICE_FAILURE_SUSPENSION'
Upgrade to 24.06.00.041  [22:02:26]: Bug 30955 - Move existing list notices to new lists category
        Moved SHARE_ACCEPT notice to lists module
        Moved SHARE_INVITE notice to lists module
        Moved LIST notice to lists module
Upgrade to 24.06.00.042  [22:02:26]: Bug 37969 - Add nor language code
        Added nor language code
Upgrade to 24.06.00.043  [22:02:26]: Bug 38193 - Add cancellation_reason field to bookings table
        Added column 'bookings.cancellation_reason'
Upgrade to 24.06.00.044  [22:02:26]: Bug 28833 - Speed up holds queue builder via parallel processing
        Added new system preference 'HoldsQueueParallelLoopsCount'
Upgrade to 24.06.00.045  [22:02:26]: Bug 35906 - Add bookable column on itemtypes table
        Added column 'itemtypes.bookable'
        Updated column 'items.bookable' allow nullable
        Updated column 'deleteditems.bookable' allow nullable
Upgrade to 24.06.00.046  [22:02:26]: Bug 38222 - Add cancellation reasons to bookings
        Added BOOKING_CANCELLATION authorised value category
Upgrade to 24.06.00.047  [22:02:26]: Bug 35659 - OAI-PMH harvester
        Added new table 'oai_servers'
        Added new table 'import_oai_biblios'
        Added new table 'import_oai_authorities'
        Updated manage_search_targets permission description
        Added OAI-PMH:HarvestEmailReport system preference
        Added OAI_HARVEST_REPORT letter
Upgrade to 24.06.00.048  [22:02:27]: Bug 33484 - Add state save as an option to datatables
        Added column 'tables_settings.default_save_state'
        Added column 'tables_settings.default_save_state_search'
Upgrade to 24.06.00.049  [22:02:27]: Bug 38274 - Fix typo in Arabic language description
        Updated Arabic language description
Upgrade to 24.06.00.050  [22:02:27]: Bug 30648 - Store biblionumber of deleted records in old_reserves
        Added column 'reserves.deleted_biblionumber'
        Added column 'old_reserves.deleted_biblionumber'
Upgrade to 24.06.00.051  [22:02:27]: Bug 14180 - Add system preference AlwaysLoadCheckoutsTable
        Added new system preference 'AlwaysLoadCheckoutsTable'
Upgrade to 24.06.00.052  [22:02:27]: Bug 35305 - Add XSLT for authority details display in staff interface
        Added new system preference 'AuthorityXSLTDetailsDisplay'
Upgrade to 24.06.00.053  [22:02:27]: Bug 37511 - Add a new column p_cs_precedes to the table currency
        Added column 'currency.p_cs_precedes'
Upgrade to 24.06.00.054  [22:02:27]: Bug 35570 - Update 'FreeForm' ILL backend to 'Standard'
Upgrade to 24.06.00.055  [22:02:27]: Bug 33462 - Force password reset for new patrons entered by staff
        Added new system preference 'ForcePasswordResetWhenSetByStaff'
        Added column 'categories.force_password_reset_when_set_by_staff'
Upgrade to 24.06.00.056  [22:02:27]: Bug 36822 - Sanitize borrowers.updated_on
Upgrade to 24.06.00.057  [22:02:27]: Bug 22421 - Add issue constraints to accountlines
        Added column 'accountlines.old_issue_id'
        Added constraint 'accountlines.old_issues'
        Updated 'accountlines.old_issue_id' from 'old_issues'
        Fixed 'accountlines.issue_id' where missing from issues
        Added constraint 'accountlines.issues'
        Added old_issue_id to accountlines and set up appropriate constraints)
Upgrade to 24.06.00.058  [22:02:27]: Bug 28633 - Add preferred_name to borrowers table
        Added column 'borrowers.preferred_name'
        Added column 'deletedborrowers.preferred_name'
        Added column 'borrower_modifications.preferred_name'
        Added 'preferred_name' to DefaultPatronSearchFields
        Initially set 'preferred_name' to 'firstname'
Upgrade to 24.06.00.059  [22:02:27]: Bug 37221 - Add new system preference OPACOverDrive
        Added new system preference 'OPACOverDrive'
Upgrade to 24.06.00.060  [22:02:27]: Bug 33766 - Add system preference to determine label of userid input on login form
        Added new system preference 'OPACLoginLabelTextContent'
Upgrade to 24.06.00.061  [22:02:27]: Bug 38011 - Add missing foreign key to subscription table
        Added new foreign key 'subscription_ibfk_4'
Upgrade to 24.06.00.062  [22:02:27]: Bug 34355 - Add a table to allow creation of MARC order accounts and a system preference to activate it
        Added new table 'marc_order_accounts'
        Added new system preference 'MarcOrderingAutomation'
        Added new permission 'marc_order_manage'
Upgrade to 24.06.00.063  [22:02:27]: Bug 33641 - Added issues.checkin_library and old_issues.checkin_library
        Added column 'issues.checkin_library'
        Added column 'old_issues.checkin_library'
Upgrade to 24.06.00.064  [22:02:27]: Bug 38436 - Adjust column names for holdings tables in the table settings
        Column names renamed
Upgrade to 24.11.00.000  [22:02:27]: Koha 24.11.00 release
Upgrade to 24.11.00.001  [22:02:27]: Bug 37292 - Add index on 'oauth_access_tokens.expires'
        Added index on 'oauth_access_tokens.expires'
Upgrade to 24.11.00.002  [22:02:27]: Bug 38522 - Increase erm_agreements.license_info length
        Updated erm_agreements.license_info to mediumtext.
Upgrade to 24.11.01.000  [22:02:27]: Koha 24.11.01 release
Upgrade to 24.11.02.000  [22:02:27]: Koha 24.11.02 release
```
