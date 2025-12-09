# Code Changes for google-cloudplatform-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'google-cloudplatform-json-app-activity-success-googleapismethodname') && !containsAny(toLower(event_category), 'data_access', 'system_event', 'policy') && !InList(toLower(operation), 'listroles', 'uploadserviceaccountkey', 'generateaccesstoken', 'buckets.list', 'objects.list', 'objects.get', 'objects.create', 'objects.delete', 'buckets.create', 'instances.list', 'instances.aggregatedlist', 'snapshots.list', 'disks.list', 'disks.aggregatedlist', 'instances.getscreenshot', 'cloudfunctionsservice.createfunction', 'roles.list', 'roles.querygrantableroles') |