# Code Changes for cisco-ie-cef-email-response (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'message_id', 'time'] |
| edit_regex_field | additional_info |  | ['MID ({message_id}({alert_id}\d+)) ({additional_info}[^"]+?)\s\w+='] |
| edit_regex_field | alert_id |  | ['MID ({message_id}({alert_id}\d+)) ({additional_info}[^"]+?)\s\w+='] |
| added_regex_field | message_id |  | ['MID ({message_id}({alert_id}\d+)) ({additional_info}[^"]+?)\s\w+='] |
| removed_attribute | DupFields |  | N/A |