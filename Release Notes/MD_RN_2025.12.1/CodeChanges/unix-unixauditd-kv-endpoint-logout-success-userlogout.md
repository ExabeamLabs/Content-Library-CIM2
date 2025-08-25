# Code Changes for unix-unixauditd-kv-endpoint-logout-success-userlogout (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | [' msg=', ' msg=audit(', ' res=success', ' type=USER_LOGOUT'] | [' msg=', ' res=success', 'USER_LOGOUT', 'audit'] |