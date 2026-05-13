# Code Changes for imprivata-i-str-app-login-fail-radiushost (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "imprivata-i-str-app-login-fail-radiushost", "Vendor": "Imprivata", "Product": "Imprivata", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["]: Login Failure to RADIUS Host,"], "Fields": ["\d\d:\d\d:\d\d ({host}[\w\-.]+) ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)", "({operation}Login Failure to RADIUS Host),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?", "Login Failure to RADIUS Host,([^,]+,){2}({user}[\w\.\-\!\#\^\~]{1,40}\$?),({domain}[^,]+)"], "ParserVersion": "v1.0.0"} |