# Code Changes for unix-unix-kv-endpoint-notification-success-powerpath (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| added_parser | N/A | N/A | {"Name": "unix-unix-kv-endpoint-notification-success-powerpath", "ParserVersion": "v1.0.0", "Vendor": "Unix", "Product": "Unix", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": [" PowerPath: ", " MPAPI: "], "Fields": ["\d\d:\d\d:\d\d(\.\S+)?\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*({host}[^\s]+)\s*PowerPath:", "\sPowerPath:\s*({additional_info}.+?)\s*$"]} |