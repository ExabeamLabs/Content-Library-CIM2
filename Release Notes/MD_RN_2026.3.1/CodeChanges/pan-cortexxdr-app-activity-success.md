# Code Changes for pan-cortexxdr-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'pan-cortex-cef-app-login-success-loginsuccess') && !InList(toLower(operation), 'login') |