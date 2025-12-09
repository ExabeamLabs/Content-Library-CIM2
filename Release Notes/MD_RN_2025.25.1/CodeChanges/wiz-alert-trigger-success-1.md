# Code Changes for wiz-alert-trigger-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'wiz-w-json-alert-trigger-success-virtualmachine', 'wiz-w-json-alert-trigger-success-cloudevents') && exists(alert_severity) && !InList(toLower(alert_severity), 'low', 'informational') |