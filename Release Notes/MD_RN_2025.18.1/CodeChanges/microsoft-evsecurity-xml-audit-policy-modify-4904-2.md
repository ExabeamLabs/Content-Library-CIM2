# Code Changes for microsoft-evsecurity-xml-audit-policy-modify-4904-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)', 'SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |