# Code Changes for rstudio-rserver-sk4-app-login-success-authlogin (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "rstudio-rserver-sk4-app-login-success-authlogin", "Vendor": "RStudio", "Product": "RStudio Server", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "Conditions": [", auth_login,", "-rstudio-server/sessions", "\"logger.account\":\""], "Fields": ["timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\"", "({event_name}auth_login)", "message\":\"({additional_info}[^,]+),\s\\?\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?\""]} | N/A |