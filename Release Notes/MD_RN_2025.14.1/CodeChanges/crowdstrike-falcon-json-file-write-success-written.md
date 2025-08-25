# Code Changes for crowdstrike-falcon-json-file-write-success-written (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_attribute | activity_type | ['file-write:success'] | ['app-activity:success', 'file-write:success'] |
| edit_attribute | legacy_activity_type | ['usb-write'] | ['app-activity', 'file-write'] |
| edit_attribute | Platform | ['Falcon'] | ['Falcon', 'Linux', 'MacOS', 'Windows'] |