# Code Changes for unix-unix-str-endpoint-notification-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'host', 'process_id', 'process_name', 'time'] |
| added_regex_field | host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+)\s'] |
| added_regex_field | time |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+)\s'] |