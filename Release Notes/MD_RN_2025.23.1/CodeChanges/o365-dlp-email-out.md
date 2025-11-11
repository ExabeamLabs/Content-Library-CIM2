# Code Changes for o365-dlp-email-out (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'alert_name', 'alert_type', 'app', 'bytes', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_subject', 'first_name', 'full_name', 'host', 'last_name', 'result', 'src_ip', 'src_port', 'time', 'user_agent', 'user_id', 'user_type'] |
| edit_regex_field | alert_name |  | ['"ClientInfoString\\*"+:[\s\\]*"+Client\\*=({alert_type}({alert_name}[^"\\;]+))'] |
| added_regex_field | alert_type |  | ['"ClientInfoString\\*"+:[\s\\]*"+Client\\*=({alert_type}({alert_name}[^"\\;]+))'] |
| removed_attribute | DupFields |  | N/A |