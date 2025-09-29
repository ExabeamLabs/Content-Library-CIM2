# Code Changes for unix-auditd-user-switch-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'unix-auditd-kv-user-switch-success-userrolechange') && exists(user_id) |