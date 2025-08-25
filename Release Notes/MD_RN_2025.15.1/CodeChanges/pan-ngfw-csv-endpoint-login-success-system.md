# Code Changes for pan-ngfw-csv-endpoint-login-success-system (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | time | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', 'SYSTEM,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)'] | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', ',SYSTEM,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)'] |