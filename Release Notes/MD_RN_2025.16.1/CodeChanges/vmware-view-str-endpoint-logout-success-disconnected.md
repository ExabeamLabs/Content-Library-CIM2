# Code Changes for vmware-view-str-endpoint-logout-success-disconnected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Vendor": "VMware", "Product": "VMware View", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Fields": ["\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View", "({app}View)", "(?:M|m)achine\s+({dest_host}[\w\-.]+)", "(?:U|u)ser\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))", "({operation}disconnected from machine)"], "Name": "vmware-view-str-endpoint-logout-success-disconnected", "ParserVersion": "v1.0.0", "Conditions": [" View ", " has disconnected from machine "]} |