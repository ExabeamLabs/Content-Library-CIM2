# Code Changes for google-cloudplatform-bucket-create-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'google-cloudplatform-json-app-activity-success-googleapismethodname') && EndsWithAny(toLower(operation), 'buckets.create') |