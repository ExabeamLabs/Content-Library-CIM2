# Code Changes for microsoft-o365-json-alert-trigger-success-moplabel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'app', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_recipients', 'file_name', 'message_id', 'object', 'operation', 'recipient_count', 'result', 'time'] |
| edit_regex_field | operation |  | ['Operation"*:\s*"*({alert_type}({operation}[^"]+))"*'] |
| added_regex_field | alert_type |  | ['Operation"*:\s*"*({alert_type}({operation}[^"]+))"*'] |
| removed_attribute | DupFields |  | N/A |