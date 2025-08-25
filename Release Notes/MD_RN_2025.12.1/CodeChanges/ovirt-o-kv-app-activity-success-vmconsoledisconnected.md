# Code Changes for ovirt-o-kv-app-activity-success-vmconsoledisconnected (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-vmconsoledisconnected", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: VM_CONSOLE_DISCONNECTED", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*?User ({user}[\w\.\-\!\#\^\~]{1,40}\$?) got disconnected from VM ({object}[^\s\"]+)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |