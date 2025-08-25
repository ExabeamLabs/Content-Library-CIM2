# Code Changes for pan-gp-csv-endpoint-authentication-success-authsuccess (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | time | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', 'SYSTEM,auth,[^,]+,({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),'] | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', ',SYSTEM,auth,[^,]+,({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),'] |