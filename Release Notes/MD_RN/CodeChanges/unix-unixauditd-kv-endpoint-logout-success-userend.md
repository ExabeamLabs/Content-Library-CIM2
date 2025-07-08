# Code Changes for unix-unixauditd-kv-endpoint-logout-success-userend (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | [' msg=', ' msg=audit(', ' res=', ' type=USER_END'] | [' msg=', ' res=', 'USER_END', 'audit'] |