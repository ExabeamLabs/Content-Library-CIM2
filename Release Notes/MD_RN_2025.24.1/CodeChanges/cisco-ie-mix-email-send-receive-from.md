# Code Changes for cisco-ie-mix-email-send-receive-from (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'email_address', 'message_id', 'time'] |
| edit_regex_field | alert_id |  | ['MID ({message_id}({alert_id}\d+))'] |
| added_regex_field | message_id |  | ['MID ({message_id}({alert_id}\d+))'] |
| removed_attribute | DupFields |  | N/A |