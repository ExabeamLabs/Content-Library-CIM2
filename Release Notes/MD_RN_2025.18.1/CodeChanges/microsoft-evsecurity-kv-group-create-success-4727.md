# Code Changes for microsoft-evsecurity-kv-group-create-success-4727 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?', '({time}\w{3}\s\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)'] |