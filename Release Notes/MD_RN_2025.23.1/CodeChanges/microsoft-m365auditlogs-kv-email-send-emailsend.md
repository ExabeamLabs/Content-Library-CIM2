# Code Changes for microsoft-m365auditlogs-kv-email-send-emailsend (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'message_id', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_type |  | ['cs6=.*?"EventType":"({alert_name}({alert_type}[^"]+))"'] |
| added_regex_field | alert_name |  | ['cs6=.*?"EventType":"({alert_name}({alert_type}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |