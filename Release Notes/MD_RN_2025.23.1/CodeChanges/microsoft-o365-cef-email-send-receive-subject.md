# Code Changes for microsoft-o365-cef-email-send-receive-subject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_source', 'alert_subject', 'alert_type', 'bytes', 'category', 'dest_email_address', 'dest_ip', 'dest_port', 'direction', 'email_address', 'email_recipients', 'email_subject', 'message_id', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_type |  | ['"EventType":"({alert_name}({alert_type}[^"]+))"'] |
| added_regex_field | alert_name |  | ['"EventType":"({alert_name}({alert_type}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |