# Code Changes for pan-ngfw-mix-alert-trigger-success-spywarealert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | [',THREAT,spyware,([^,]*,){26}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |