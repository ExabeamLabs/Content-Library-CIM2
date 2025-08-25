# Code Changes for microsoft-evsecurity-xml-log-clear-success-1102 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"', 'SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)'] |