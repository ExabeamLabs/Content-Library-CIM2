# Code Changes for microsoft-azure-json-file-success-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | bytes_in |  | ['"+properties"+:[^\}]+"+requestBodySize"+:\s*({bytes_in}\d+)', 'exa_json_path=$..requestBodySize,exa_regex=({bytes_in}\d+)'] |
| edit_regex_field | bytes_out |  | ['"+properties"+:[^\}]+"+responseBodySize"+:\s*({bytes_out}\d+)', 'exa_json_path=$..responseBodySize,exa_regex=({bytes_out}\d+)'] |
| edit_regex_field | time |  | ['"+time"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+', 'exa_regex="time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)'] |
| edit_attribute | activity_type |  | ['app-activity:fail', 'app-activity:success', 'file-create:fail', 'file-create:success', 'file-delete:fail', 'file-delete:success', 'file-list:fail', 'file-list:success', 'file-permission-modify:fail', 'file-permission-modify:success', 'file-permission-read:fail', 'file-permission-read:success', 'file-read:fail', 'file-read:success', 'file-rename:fail', 'file-rename:success', 'file-write:fail', 'file-write:success', 'folder-create:fail', 'folder-create:success'] |
| edit_attribute | legacy_activity_type |  | ['azure-blob-delete', 'azure-blob-read', 'azure-blob-write', 'azure-container-acl', 'azure-container-write', 'azure-general-activity', 'azure-storage-list', 'file-write'] |