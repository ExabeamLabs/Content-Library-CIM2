# Code Changes for pan-ngfw-csv-app-activity-globalprotect (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | additional_info | ['SYSTEM,(?:[^,]*,){10}"*\s*({additional_info}[^",]+?)(?:\.*"|\.\s|\.*,|\s(\d{1,3}\.){3}\d{1,3}:\d+)'] | [',SYSTEM,(?:[^,]*,){10}"*\s*({additional_info}[^",]+?)(?:\.*"|\.\s|\.*,|\s(\d{1,3}\.){3}\d{1,3}:\d+)'] |
| edit_regex_field | event_subtype | ['SYSTEM,({event_subtype}[^,]+),'] | [',SYSTEM,({event_subtype}[^,]+),'] |
| edit_regex_field | host | [',SYSTEM,([^,]*,){10}("[^"]+")?,([^,]*,){7}({device_name}({host}[^",]+))', ':\d\d:\d\d\s+({host}[\w\-\.]+)\s', 'SYSTEM,("[^"]*",|[^,]*,){18}({host}[\w\-\.]+),'] | [',SYSTEM,("[^"]*",|[^,]*,){18}({host}[\w\-\.]+),', ',SYSTEM,([^,]*,){10}("[^"]+")?,([^,]*,){7}({device_name}({host}[^",]+))', ':\d\d:\d\d\s+({host}[\w\-\.]+)\s'] |
| edit_regex_field | severity | ['SYSTEM,([^,]*,){9}({severity}[^,]+),'] | [',SYSTEM,([^,]*,){9}({severity}[^,]+),'] |
| edit_regex_field | time | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', 'SYSTEM,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),', 'SYSTEM[^"]+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)'] | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', ',SYSTEM,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),', 'SYSTEM[^"]+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)'] |