# Code Changes for unix-auditd-kv-user-switch-success-userrolechange (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | [' auid=', ' msg=audit(', ' type=USER_ROLE_CHANGE'] | [' auid=', ' msg=', 'USER_ROLE_CHANGE', 'audit'] |