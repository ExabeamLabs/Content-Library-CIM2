# Code Changes for forcepoint-dlp-cef-alert-trigger-success-dlpsyslog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'file_name', 'full_name', 'host', 'target', 'time'] |
| edit_regex_field | alert_type |  | ['caseClassification=({alert_name}({alert_type}.+?))\s*numberOfI'] |
| added_regex_field | alert_name |  | ['caseClassification=({alert_name}({alert_type}.+?))\s*numberOfI'] |
| removed_attribute | DupFields |  | N/A |