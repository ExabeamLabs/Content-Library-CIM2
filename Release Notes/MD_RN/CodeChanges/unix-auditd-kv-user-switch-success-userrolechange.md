# Code Changes for unix-auditd-kv-user-switch-success-userrolechange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | [' auid=', ' msg=audit(', ' type=USER_ROLE_CHANGE'] | [' auid=', ' msg=', 'USER_ROLE_CHANGE', 'audit'] |