# Code Changes for cisco-ie-str-email-attachment (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'attachment', 'email_attachment', 'file_ext', 'message_id'] |
| edit_regex_field | alert_id |  | ["MID ({message_id}({alert_id}\d+)) attachment '({attachment}({email_attachment}[^']+))'"] |
| edit_regex_field | email_attachment |  | ["MID ({message_id}({alert_id}\d+)) attachment '({attachment}({email_attachment}[^']+))'", "attachment '({email_attachment}[^']+\.({file_ext}[^']+))'"] |
| added_regex_field | attachment |  | ["MID ({message_id}({alert_id}\d+)) attachment '({attachment}({email_attachment}[^']+))'"] |
| added_regex_field | message_id |  | ["MID ({message_id}({alert_id}\d+)) attachment '({attachment}({email_attachment}[^']+))'"] |
| removed_attribute | DupFields |  | N/A |