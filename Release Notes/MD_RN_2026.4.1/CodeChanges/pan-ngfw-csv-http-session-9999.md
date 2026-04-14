# Code Changes for pan-ngfw-csv-http-session-9999 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['THREAT,url,([^,]*,){26}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |