# Code Changes for unix-unix-kv-endpoint-login-userstart (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | [' msg=', ' msg=audit(', ' res=', ' type=USER_START'] | [' msg=', ' msg=', ' res=', 'USER_START', 'audit'] |
| edit_regex_field | audispd_type | ['\stype=({audispd_type}USER_\S+)\s+\w+='] | ['({audispd_type}USER_\S+)\s+\w+='] |