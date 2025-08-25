# Code Changes for pan-ngfw-csv-app-notification-system (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | device_name | [',SYSTEM,([^,]*,){10}("[^"]+"),([^,]*,){7}({device_name}({host}[^,]+))', 'Deviating device:\s*({device_name}[^,]+)', 'SYSTEM,([^,]*,){18}([^,]*,)?({device_name}({host}[\w\-\.]+))"?$'] | [',SYSTEM,([^,]*,){10}("[^"]+"),([^,]*,){7}({device_name}({host}[^,]+))', ',SYSTEM,([^,]*,){18}([^,]*,)?({device_name}({host}[\w\-\.]+))"?$', 'Deviating device:\s*({device_name}[^,]+)'] |
| edit_regex_field | event_code | ['SYSTEM,([^,]*,){4}({event_code}[^,]+),'] | [',SYSTEM,([^,]*,){4}({event_code}[^,]+),'] |
| edit_regex_field | event_name | ['SYSTEM,(?:[^,]*,){10}"*({event_name}.+?)(?:\.*"|\.\s)'] | [',SYSTEM,(?:[^,]*,){10}"*({event_name}.+?)(?:\.*"|\.\s)'] |
| edit_regex_field | event_subtype | ['SYSTEM,({event_subtype}[^,]+),'] | [',SYSTEM,({event_subtype}[^,]+),'] |
| edit_regex_field | host | [',SYSTEM,([^,]*,){10}("[^"]+"),([^,]*,){7}({device_name}({host}[^,]+))', ':\d\d:\d\d (-|({host}[\w\-\.]+))\s', 'SYSTEM,([^,]*,){18}([^,]*,)?({device_name}({host}[\w\-\.]+))"?$', 'SYSTEM,([^,]*,){18}([^,]*,)?({host}[\w\-\.]+)"?$'] | [',SYSTEM,([^,]*,){10}("[^"]+"),([^,]*,){7}({device_name}({host}[^,]+))', ',SYSTEM,([^,]*,){18}([^,]*,)?({device_name}({host}[\w\-\.]+))"?$', ',SYSTEM,([^,]*,){18}([^,]*,)?({host}[\w\-\.]+)"?$', ':\d\d:\d\d (-|({host}[\w\-\.]+))\s'] |
| edit_regex_field | object | ['SYSTEM,([^,]*,){5}\s*(|({object}[^,]+)),'] | [',SYSTEM,([^,]*,){5}\s*(|({object}[^,]+)),'] |
| edit_regex_field | severity | ['SYSTEM,([^,]*,){9}({severity}[^,]+),'] | [',SYSTEM,([^,]*,){9}({severity}[^,]+),'] |