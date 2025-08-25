# Code Changes for pan-ngfw-csv-configuration-modify-success-configunauthorized (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | host | ['CONFIG,([^,]*,){17}({host}[^\s,]+)', '\d\d:\d\d:\d\d\s(?:-|({host}[^:\s]+))\s\d+,\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d,'] | [',CONFIG,([^,]*,){17}({host}[^\s,]+)', '\d\d:\d\d:\d\d\s(?:-|({host}[^:\s]+))\s\d+,\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d,'] |
| edit_regex_field | object | ['CONFIG,([^,]*,){9}\s*({object}[^,]+),'] | [',CONFIG,([^,]*,){9}\s*({object}[^,]+),'] |
| edit_regex_field | operation | ['CONFIG,([^,]*,){5}({operation}[^,]+),'] | [',CONFIG,([^,]*,){5}({operation}[^,]+),'] |
| edit_regex_field | result | ['CONFIG,([^,]*,){8}({result}[^,]+),'] | [',CONFIG,([^,]*,){8}({result}[^,]+),'] |
| edit_regex_field | time | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', 'CONFIG,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)'] | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', ',CONFIG,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)'] |
| edit_regex_field | user | ['CONFIG,.+?\d\d:\d\d:\d\d([^,]*,){4}({user}[\w\.\-\!\#\^\~]{1,40}\$?),'] | [',CONFIG,.+?\d\d:\d\d:\d\d([^,]*,){4}({user}[\w\.\-\!\#\^\~]{1,40}\$?),'] |