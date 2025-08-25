# Code Changes for microsoft-o365-cef-app-file-teams (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_attribute | activity_type | ['app-activity:fail', 'app-activity:success', 'app-login:success', 'file-delete:success', 'file-download:success', 'file-read:success', 'file-upload:success'] | ['app-activity:fail', 'app-activity:success', 'app-login:success', 'file-create:success', 'file-delete:success', 'file-download:success', 'file-read:success', 'file-upload:success'] |
| edit_attribute | legacy_activity_type | ['app-activity', 'app-activity-failed', 'app-login', 'file-delete', 'file-download', 'file-read', 'file-upload'] | ['app-activity', 'app-activity-failed', 'app-login', 'file-delete', 'file-download', 'file-read', 'file-upload', 'usb-write'] |