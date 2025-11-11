# Code Changes for microsoft-o365-sk4-alert-trigger-success-securitycompliance (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'app', 'category', 'email_address', 'malware_url', 'operation', 'result', 'time'] |
| edit_regex_field | alert_name |  | ['"Name":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| added_regex_field | alert_subject |  | ['"Name":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| removed_attribute | DupFields |  | N/A |