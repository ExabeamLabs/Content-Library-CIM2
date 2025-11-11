# Code Changes for microsoft-azureadip-mix-alert-trigger-success-unfamiliarlocation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'domain', 'email_address', 'full_name', 'location', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| edit_regex_field | alert_name |  | ['"title":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| added_regex_field | alert_subject |  | ['"title":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| removed_attribute | DupFields |  | N/A |