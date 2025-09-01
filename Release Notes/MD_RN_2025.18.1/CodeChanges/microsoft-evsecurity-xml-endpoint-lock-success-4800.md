# Code Changes for microsoft-evsecurity-xml-endpoint-lock-success-4800 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['<EventTime>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)', '<TimeCreated SystemTime(\\)?=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'] |