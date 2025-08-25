# Code Changes for unix-unixauditd-kv-endpoint-logout-success-userend (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | [' msg=', ' msg=audit(', ' res=', ' type=USER_END'] | [' msg=', ' res=', 'USER_END', 'audit'] |