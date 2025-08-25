# Code Changes for ovirt-o-kv-app-activity-success-vmsetticket (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-vmsetticket", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: VM_SET_TICKET", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*?User ({user}[\w\.\-\!\#\^\~]{1,40}\$?) initiated console session for VM ({object}[^\s\"]+)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |