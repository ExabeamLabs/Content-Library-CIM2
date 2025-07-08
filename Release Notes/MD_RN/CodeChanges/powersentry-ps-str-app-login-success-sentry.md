# Code Changes for powersentry-ps-str-app-login-success-sentry (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "powersentry-ps-str-app-login-success-sentry", "Vendor": "PowerSentry", "Product": "PowerSentry", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" [Sentry", "\" logged in --"], "Fields": ["\d\d:\d\d:\d\d ({host}[^\s]+) \[({src_host}[^\]]+)\].+?User \"({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "connection source ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? using ({protocol}[^\s]+)"], "ParserVersion": "v1.0.0"} | N/A |