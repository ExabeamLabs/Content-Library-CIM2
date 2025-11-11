# Code Changes for microsoft-azureadip-json-alert-trigger-success-anonymouslogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'app', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'full_name', 'incident_status', 'location', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user', 'user_upn'] |
| edit_regex_field | alert_name |  | ['"title":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| added_regex_field | alert_subject |  | ['"title":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |