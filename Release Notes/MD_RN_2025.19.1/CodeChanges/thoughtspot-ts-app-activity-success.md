# Code Changes for thoughtspot-ts-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'thoughtspot-ts-json-app-activity-success-type') && !InList(operation, 'USERS_MODIFIED', 'LOGIN_SUCCESSFUL', 'LOGOUT_SUCCESSFUL', 'USER_GROUP_MODIFIED', 'LOGIN_FAILED', 'USER_GROUPS_CREATED', 'USERS_CREATED', 'USERS_DELETED', 'UPDATE_PASSWORD') |