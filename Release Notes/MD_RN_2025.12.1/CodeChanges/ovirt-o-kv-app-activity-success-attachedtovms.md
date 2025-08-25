# Code Changes for ovirt-o-kv-app-activity-success-attachedtovms (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-attachedtovms", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: USER_FINISHED_REMOVE_DISK_ATTACHED_TO_VMS", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*? Disk ({object}[^\s\"]+).*? was successfully removed from domain ({resource}[^\s]+) \(User ({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |