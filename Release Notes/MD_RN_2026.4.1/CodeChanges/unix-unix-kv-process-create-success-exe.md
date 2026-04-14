# Code Changes for unix-unix-kv-process-create-success-exe (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({host}[\w\-.]+)\s*(vcsa-audit|audispd:)', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w\-.]+)', '\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s({host}[\w\-.]+)\saudit', '\w+\s*\d{1,2} \d\d:\d\d:\d\d\s+({host}[\w\-.]+)'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'process-create:success', 'syscall-execute:fail', 'syscall-execute:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'process-created', 'process-created-failed'] |