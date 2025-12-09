# Code Changes for symantec-endpointprotection-kv-app-notification-eventdescription (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'category', 'event_name', 'host', 'priority', 'time'] |
| edit_regex_field | host |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s+SymantecServer:'] |
| edit_regex_field | time |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s+SymantecServer:', 'Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)'] |
| added_regex_field | alert_severity |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s+SymantecServer:'] |
| added_regex_field | priority |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s+SymantecServer:'] |