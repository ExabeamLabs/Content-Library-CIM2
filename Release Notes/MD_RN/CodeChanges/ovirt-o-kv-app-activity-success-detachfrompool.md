# Code Changes for ovirt-o-kv-app-activity-success-detachfrompool (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-detachfrompool", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: USER_DETACH_STORAGE_DOMAIN_FROM_POOL", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*?User(:)? ({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\)|\s|\.\s|\.$)", "EVENT_ID:.*? Storage Domain ({object}[^\s\"]+) was detached from Data Center Exabeam by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\)|\s|\.\s|\.$)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |