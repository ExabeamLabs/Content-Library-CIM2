# Code Changes for microsoft-evsecurity-json-user-unlock-success-4767-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code |  | ['"event_id"+:({event_code}\d+)', '"record_id"+:({event_id}({event_code}\d+))'] |
| edit_regex_field | event_id |  | ['"record_id"+:({event_id}({event_code}\d+))'] |
| removed_attribute | DupFields |  | N/A |