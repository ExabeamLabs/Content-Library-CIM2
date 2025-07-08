# Code Changes for ovirt-o-kv-app-activity-success-networkaddvminterface (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-networkaddvminterface", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: NETWORK_ADD_VM_INTERFACE", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*? was added to VM ({object}[^\s\"]+?)\.?\s\(User: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\)|\s|\.\s|\.$)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |