# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4624-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['"TimeCreated":".*?({time}\d{1,13}).*?",', '"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)', '"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"', '({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))', '({time}\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s\d{4})\s+4624\s+Microsoft-Windows-Security-Auditing', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)', 'TimeGenerated=({time}\d{10})', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |