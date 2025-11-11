# Code Changes for q-microsoft-security-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'dest_ip', 'domain', 'email_address', 'file_name', 'full_name', 'incident_status', 'location', 'malware_url', 'src_host', 'src_ip', 'time', 'user', 'user_upn'] |
| edit_regex_field | alert_name |  | ['"title"+:\s*"+({alert_subject}({alert_name}[^"]+))"'] |
| added_regex_field | alert_subject |  | ['"title"+:\s*"+({alert_subject}({alert_name}[^"]+))"'] |