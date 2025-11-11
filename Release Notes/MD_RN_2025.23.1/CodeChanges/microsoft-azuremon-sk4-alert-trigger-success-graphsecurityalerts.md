# Code Changes for microsoft-azuremon-sk4-alert-trigger-success-graphsecurityalerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'domain', 'email_address', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['"title":"({alert_type}({alert_name}[^"]+?))(\\u200b)?"'] |
| added_regex_field | alert_type |  | ['"title":"({alert_type}({alert_name}[^"]+?))(\\u200b)?"'] |
| removed_attribute | DupFields |  | N/A |