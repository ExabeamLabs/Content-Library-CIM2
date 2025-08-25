# Code Changes for powersentry-ps-str-app-logout-success-loggedout (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "powersentry-ps-str-app-logout-success-loggedout", "Vendor": "PowerSentry", "Product": "PowerSentry", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" [Sentry", "\" logged out --"], "Fields": ["\d\d:\d\d:\d\d ({host}[^\s]+) \[({src_host}[^\]]+)\].+?User \"({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "connection source ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? using ({protocol}[^\s]+)"]} | N/A |