# Code Changes for pan-ngfw-csv-alert-trigger-success-file (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_name |  | ['THREAT,([^,]*,){46}("[^"]+")?,("[^"]+")?,(("[^"]+")|([^,]*)),([^,]*,){6}({device_name}({host}[^",]+))'] |
| edit_regex_field | host |  | ['THREAT,([^,]*,){46}("[^"]+")?,("[^"]+")?,(("[^"]+")|([^,]*)),([^,]*,){6}({device_name}({host}[^",]+))', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |