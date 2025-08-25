# Code Changes for helpsystems-powertechiam-kv-endpoint-login-success-loginok (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| added_parser | N/A | N/A | {"Name": "helpsystems-powertechiam-kv-endpoint-login-success-loginok", "Vendor": "HelpSystems", "Product": "Powertech Identity and Access Manager", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss", "Conditions": ["login - login_ok", "Successful login"], "Fields": ["clientTime=\\"*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z\\"*", "authHost=\\"*({host}[^\\"]+)\\"", "user=\\"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\""], "DupFields": ["host->dest_host"], "ParserVersion": "v1.0.0"} |