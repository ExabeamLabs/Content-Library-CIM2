# Code Changes for google-cloudplatform-file-read-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'google-cloudplatform-json-app-activity-success-googleapismethodname') && EndsWithAny(toLower(operation), 'objects.get') |