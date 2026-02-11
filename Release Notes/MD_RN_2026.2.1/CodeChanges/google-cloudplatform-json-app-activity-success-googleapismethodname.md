# Code Changes for google-cloudplatform-json-app-activity-success-googleapismethodname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | region |  | ['"resource"+:[^\}]*labels[^\}]*"+location"+:\s*"+({region}[^"\\\/\}]+)"+', '"resource":"({resource}[^"]+)","resource"+:[^\}]*labels[^\}]*"+region"+:\s*"+({region}[^"\\\/\}]+)"+'] |
| edit_regex_field | resource |  | ['"resource":"({resource}[^"]+)","resource"+:[^\}]*labels[^\}]*"+region"+:\s*"+({region}[^"\\\/\}]+)"+', '"resource":({resource}[^\$]+?}}),"destinationServiceName":', '"resource":\s*({resource}[^]]+?\s*"type":"[^"]+"}),'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'app-login:fail', 'bucket-create:success', 'bucket-list:success', 'disk-list:success', 'endpoint-list:success', 'endpoint-screenshot:success', 'file-delete:success', 'file-list:success', 'file-read:success', 'file-write:success', 'function-write:success', 'role-list:success', 'snapshot-list:success', 'user-key-create:success'] |
| edit_attribute | legacy_activity_type |  | ['failed-app-login', 'file-delete', 'gcp-bucket-create', 'gcp-compute-list', 'gcp-function-write', 'gcp-general-activity', 'gcp-instance-screenshot', 'gcp-role-list', 'gcp-serviceaccount-creds-write', 'gcp-storage-list', 'gcp-storageobject-read', 'gcp-storageobject-write'] |