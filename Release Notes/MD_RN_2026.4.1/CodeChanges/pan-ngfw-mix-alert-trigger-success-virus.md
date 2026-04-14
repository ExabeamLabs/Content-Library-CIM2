# Code Changes for pan-ngfw-mix-alert-trigger-success-virus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"host":\{[^=]*?"name":"({host}[^"]+)"[^=]*?\}', '({host}[\w\-\.]+)\s+\d+,[^,]*,[^,]*,THREAT,virus,', ',THREAT(,[^,]*){40},("[^"]*",)([^,]*,){3}("[^"]*",){5}([^,]*,){6}({host}[^,]+).', ',THREAT,([^,]*,){55}(|({host}[^,]+)),', ',THREAT,virus,([^,]*,){26}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |