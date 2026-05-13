# Code Changes for pan-ngfw-csv-alert-trigger-success-file (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_name |  | ['THREAT,([^,]*,){46}("[^"]+")?,("[^"]+")?,(("[^"]+")|([^,]*)),([^,]*,){6}(\d|({device_name}[^",]+))'] |
| edit_regex_field | host |  | ['\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |