# Code Changes for ovirt-o-kv-app-activity-success-userupdatevm (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "ovirt-o-kv-app-activity-success-userupdatevm", "Vendor": "oVirt", "Product": "oVirt", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["EVENT_ID: USER_UPDATE_VM", "ovirt"], "Fields": ["({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt", "EVENT_ID:\s*({operation}[^\(\)]+)", "EVENT_ID:.*?VM ({object}[^\s\"]+) configuration was updated by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\)|\s|\.\s|\.$)", "({app}ovirt)"], "ParserVersion": "v1.0.0"} | N/A |