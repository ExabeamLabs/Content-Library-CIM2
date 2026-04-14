# Code Changes for pan-ngfw-csv-alert-trigger-success-url (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_name |  | ['THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[\w.-]+))'] |
| edit_regex_field | host |  | ['THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[\w.-]+))', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\s+({host}[\w.-]+)\s+\d+,.+?,.+?,THREAT,', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |