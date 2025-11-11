# Code Changes for microsoft-o365-json-email-send-success-messagetrace (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_subject', 'result', 'src_ip', 'src_port', 'time', 'time_ended', 'time_started'] |
| edit_regex_field | email_subject |  | ['"d:Subject"":\s*"({alert_name}({email_subject}[^"]+))"'] |
| added_regex_field | alert_name |  | ['"d:Subject"":\s*"({alert_name}({email_subject}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |