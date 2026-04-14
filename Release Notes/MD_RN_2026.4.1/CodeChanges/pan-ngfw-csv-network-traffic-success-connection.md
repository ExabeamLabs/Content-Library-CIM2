# Code Changes for pan-ngfw-csv-network-traffic-success-connection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))', '\d+:\d+:\d\d[\+-]\d+:\d+\s+({host}[\w.-]+)\s', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,'] |