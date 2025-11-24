# Code Changes for unix-unix-cef-email-send-receive-sendmail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_recipients', 'host', 'num_recipients', 'protocol', 'result', 'time'] |
| edit_regex_field | alert_name |  | ['CEF:([^\|]*\|){4}({alert_type}({alert_name}[^\|]+))'] |
| added_regex_field | alert_type |  | ['CEF:([^\|]*\|){4}({alert_type}({alert_name}[^\|]+))'] |
| removed_attribute | DupFields |  | N/A |