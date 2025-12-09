# Code Changes for microsoft-evsecurity-kv-group-modify-success-4735 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | Product |  | Event Viewer - Security |
| edit_regex_field | host |  | ['"(?i)Computer(Name)?":\s*"({host}[^"]+)"', '"(?i)HostName":\s*"({host}[^"]+)"', '({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s', '\sComputer:\s+({host}[\w\-.]+)\s'] |
| edit_regex_field | time |  | ['({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s', '({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))', '({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)', 'EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"', '\srt=({time}\d{13})'] |