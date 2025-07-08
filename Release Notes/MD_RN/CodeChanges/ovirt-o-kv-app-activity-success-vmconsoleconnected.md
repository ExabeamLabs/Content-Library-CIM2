# Code Changes for ovirt-o-kv-app-activity-success-vmconsoleconnected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-vmconsoleconnected", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: VM_CONSOLE_CONNECTED", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*?User ({user}[\w\.\-\!\#\^\~]{1,40}\$?) is connected to VM ({object}[^\s\"]+)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |