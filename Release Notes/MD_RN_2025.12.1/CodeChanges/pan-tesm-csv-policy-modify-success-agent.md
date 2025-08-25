# Code Changes for pan-tesm-csv-policy-modify-success-agent (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Vendor": "Palo Alto Networks", "TimeFormat": ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd yyyy HH:mm:ss"], "Fields": ["\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({host}[^,]+),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),", "((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"], "DupFields": ["host->dest_host"], "Name": "pan-tesm-csv-policy-modify-success-agent", "Product": "Traps Endpoint Security Manager", "ParserVersion": "v1.0.0", "Conditions": [",Traps", ",Agent Policy Changed,"]} | N/A |