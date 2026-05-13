# Code Changes for imprivata-i-str-user-lock-primarylockout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "imprivata-i-str-user-lock-primarylockout", "Vendor": "Imprivata", "Product": "Imprivata", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["]: Primary Lock-Out,"], "Fields": ["\d\d:\d\d:\d\d ({host}[\w\-.]+) ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)", "({operation}Primary Lock-Out),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?", "Primary Lock-Out,([^,]+,){2}({user}[\w\.\-\!\#\^\~]{1,40}\$?),({domain}[^,]+)"], "ParserVersion": "v1.0.0"} |