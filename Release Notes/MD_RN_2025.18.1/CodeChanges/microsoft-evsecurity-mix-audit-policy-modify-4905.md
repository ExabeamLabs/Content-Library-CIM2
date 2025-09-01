# Code Changes for microsoft-evsecurity-mix-audit-policy-modify-4905 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)', '({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)', 'Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?(am|AM|pm|PM|({host}[\w.\-]+))', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)', 'TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)".', '\srt=({time}\d{13})'] |