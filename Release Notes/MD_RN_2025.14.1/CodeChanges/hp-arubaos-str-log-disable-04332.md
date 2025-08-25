# Code Changes for hp-arubaos-str-log-disable-04332 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| added_parser | N/A | N/A | {"Vendor": "HP", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Fields": ["\d\d:\d\d:\d\d\s({host}\S+)\s({event_code}\S+)\s({event_name}[^\s:]+):\s*({additional_info}[^\n\"]+?)\s*$", "port\s({dest_port}\d+)", "User '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'", "from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"], "Name": "hp-arubaos-str-log-disable-04332", "ParserVersion": "v1.0.0", "Product": "ArubaOS", "Conditions": [" 04332 ", " mgr:"]} |