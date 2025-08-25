# Code Changes for vmware-view-str-app-authentication-fail-denied (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Vendor": "VMware", "Product": "VMware View", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Fields": ["\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View", "({app}View)", "(?:M|m)achine\s+({dest_host}[\w\-.]+)", "(?:U|u)ser\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))", "({additional_info}View [^\"]+?)\s*$", "({operation}access denied)"], "Name": "vmware-view-str-app-authentication-fail-denied", "ParserVersion": "v1.0.0", "Conditions": [" View ", " access denied for user "]} |