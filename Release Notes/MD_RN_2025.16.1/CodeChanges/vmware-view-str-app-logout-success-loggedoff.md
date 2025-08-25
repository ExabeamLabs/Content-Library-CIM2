# Code Changes for vmware-view-str-app-logout-success-loggedoff (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Vendor": "VMware", "Product": "VMware View", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Fields": ["\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View", "({app}View)", "(?:M|m)achine\s+({dest_host}[\w\-.]+)", "(?:U|u)ser\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))", "({additional_info}User\s[^\"]+?)\s*$", "({operation}logged off)"], "Name": "vmware-view-str-app-logout-success-loggedoff", "ParserVersion": "v1.0.0", "Conditions": [" View ", " has logged off from "]} |