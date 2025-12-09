# Code Changes for hp-arubaos-str-ssh-start-session (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "hp-arubaos-str-ssh-start-session", "ParserVersion": "v1.0.0", "Vendor": "HP", "Product": "ArubaOS", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss", "Conditions": ["SSH session", " from "], "Fields": ["({time}\d+-\d+-\d+T\d+:\d+:\d+)\.\d+[\+\-]\d+:\d+\s+({host}\S+)\s({app}\S+)\s({PID}\S+)\s", "Event\|({event_code}\d+)\|({severity}\w+)\|({sub_category}\w+)\|\S+\|\s*({result}[^$]+)", "User\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"]} |