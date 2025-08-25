# Code Changes for vmware-horizon-str-endpoint-authentication-success-allocated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "vmware-horizon-str-endpoint-authentication-success-allocated", "ParserVersion": "v1.0.0", "Vendor": "VMware", "Product": "VMware Horizon", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "Conditions": [" View ", "allocated machine"], "Fields": ["\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)", "({app}View)", "User\s+(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "({event_name}({operation}requested Pool [^,]+).+?)[\s\"]*$"]} |