# Code Changes for unix-unix-str-endpoint-notification-success-avahidaemon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | TimeFormat |  | MMM dd HH:mm:ss |
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'host', 'process_id', 'process_name', 'time'] |
| added_regex_field | host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+)\s'] |
| added_regex_field | time |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({host}[\w.\-]+)\s'] |