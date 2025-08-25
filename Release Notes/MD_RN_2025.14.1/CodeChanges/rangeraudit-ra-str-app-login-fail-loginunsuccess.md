# Code Changes for rangeraudit-ra-str-app-login-fail-loginunsuccess (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "rangeraudit-ra-str-app-login-fail-loginunsuccess", "Vendor": "RangerAudit", "Product": "RangerAudit", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["ranger", "Login Unsuccessful:", "Ip Address:"], "Fields": ["\[({host}[^\]]+)", "({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)", "Ip Address:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*\|\s*({failure_reason}.+?)\s*$", "({app}ranger)"], "ParserVersion": "v1.0.0"} | N/A |