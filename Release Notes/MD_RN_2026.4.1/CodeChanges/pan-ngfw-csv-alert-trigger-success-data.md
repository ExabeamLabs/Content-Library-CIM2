# Code Changes for pan-ngfw-csv-alert-trigger-success-data (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | [',THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){27}({device_name}({host}[\w\-\.]+))(,|$)', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |