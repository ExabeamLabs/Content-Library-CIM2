# Code Changes for microsoft-o365-sk4-email-send-fail-outbound (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_type', 'bytes', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'email_user', 'message_id', 'result', 'spam_score', 'time'] |
| edit_regex_field | alert_type |  | ['"EventType":"({result}({alert_name}({alert_type}[^"]+)))"'] |
| added_regex_field | alert_name |  | ['"EventType":"({result}({alert_name}({alert_type}[^"]+)))"'] |
| added_regex_field | result |  | ['"EventType":"({result}({alert_name}({alert_type}[^"]+)))"'] |
| removed_attribute | DupFields |  | N/A |