# Code Changes for ovirt-o-kv-app-activity-success-userstopvm (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-userstopvm", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: USER_STOP_VM", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*? VM ({object}[^\s\"]+) powered off by ({user}[\w\.\-\!\#\^\~]{1,40}\$?) \(({resource}[^\)]+)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |