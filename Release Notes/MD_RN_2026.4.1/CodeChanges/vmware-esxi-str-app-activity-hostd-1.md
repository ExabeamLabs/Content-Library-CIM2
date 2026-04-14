# Code Changes for vmware-esxi-str-app-activity-hostd-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\s', '\s*({host}[\w.-]+)\s*Hostd:'] |