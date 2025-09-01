# Code Changes for microsoft-evsecurity-str-registry-create-success-4657 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['({event_code}\d+)\|\s+devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+({event_code}4657)', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'] |