# Code Changes for vmware-view-str-app-logout-success-loggedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "vmware-view-str-app-logout-success-loggedout", "ParserVersion": "v1.0.0", "Vendor": "VMware", "Product": "VMware View", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["View User", " has logged out"], "Fields": ["\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View User", "View User\s+(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "({app}View)"]} |