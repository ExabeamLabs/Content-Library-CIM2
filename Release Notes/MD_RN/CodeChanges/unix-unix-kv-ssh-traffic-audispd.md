# Code Changes for unix-unix-kv-ssh-traffic-audispd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | [' msg=audit(', ' type=USER_', ' uid='] | [' msg=', ' uid=', 'USER_', 'audit'] |