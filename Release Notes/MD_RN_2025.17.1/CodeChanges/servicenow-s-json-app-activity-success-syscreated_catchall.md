# Code Changes for servicenow-s-json-app-activity-success-syscreated_catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "servicenow-s-json-app-activity-success-syscreated_catchall", "Vendor": "ServiceNow", "Product": "ServiceNow", "ParserVersion": "v1.0.0", "ExtractionType": "json", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["\"sys_created_on\":", "\"sys_created_by\":", "\"level\":", "\"message\":"], "Fields": ["exa_json_path=$.sys_created_on,exa_field_name=time", "exa_json_path=$.message,exa_field_name=additional_info", "exa_json_path=$.level,exa_field_name=severity", "exa_json_path=$.sys_created_by,exa_field_name=user"]} |