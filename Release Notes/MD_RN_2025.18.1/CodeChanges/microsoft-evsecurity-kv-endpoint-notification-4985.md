# Code Changes for microsoft-evsecurity-kv-endpoint-notification-4985 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)', '({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)', '({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)\s', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)', 'TimeGenerated=({time}\d{13})', '\Wrt=({time}\d+)'] |