# Code Changes for unix-unix-kv-endpoint-activity-success-postfix (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'end_time', 'event_category', 'event_name', 'object', 'start_time', 'time', 'user'] |
| edit_regex_field | start_time |  | ['time=({time}({start_time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d))'] |
| added_regex_field | time |  | ['time=({time}({start_time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d))'] |
| removed_attribute | DupFields |  | N/A |