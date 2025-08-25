# Code Changes for vmware-view-str-endpoint-login-success-reconnected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Vendor": "VMware", "Product": "VMware View", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Fields": ["\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View", "({app}View)", "(?:M|m)achine\s+({dest_host}[\w\-.]+)", "(?:U|u)ser\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))", "({additional_info}reconnected to [^\"]+?)\s*$", "({operation}reconnected to machine)"], "Name": "vmware-view-str-endpoint-login-success-reconnected", "ParserVersion": "v1.0.0", "Conditions": [" View ", " has reconnected to machine "]} |