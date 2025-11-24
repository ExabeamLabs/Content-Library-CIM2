# Code Changes for unix-unix-str-cron-session-success-sessionopened (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'host', 'process_id', 'process_name', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({dest_host}({host}[\w.\-]+))\s'] |
| edit_regex_field | time |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({dest_host}({host}[\w.\-]+))\s'] |
| added_regex_field | dest_host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({dest_host}({host}[\w.\-]+))\s'] |
| removed_attribute | DupFields |  | N/A |