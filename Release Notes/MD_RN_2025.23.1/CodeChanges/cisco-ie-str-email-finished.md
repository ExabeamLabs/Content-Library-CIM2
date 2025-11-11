# Code Changes for cisco-ie-str-email-finished (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'message_id', 'result', 'time'] |
| edit_regex_field | alert_id |  | ['Message finished MID ({message_id}({alert_id}\d+)) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)'] |
| edit_regex_field | result |  | ['Message finished MID ({message_id}({alert_id}\d+)) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)'] |
| added_regex_field | message_id |  | ['Message finished MID ({message_id}({alert_id}\d+)) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)'] |
| removed_attribute | DupFields |  | N/A |