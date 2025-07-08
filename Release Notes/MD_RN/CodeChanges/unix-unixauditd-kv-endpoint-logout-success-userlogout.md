# Code Changes for unix-unixauditd-kv-endpoint-logout-success-userlogout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | [' msg=', ' msg=audit(', ' res=success', ' type=USER_LOGOUT'] | [' msg=', ' res=success', 'USER_LOGOUT', 'audit'] |