# Code Changes for unix-unix-ssh-traffic-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'unix-unix-kv-ssh-traffic-sshuserauth', 'unix-unix-kv-endpoint-login-sshdauth', 'unix-unix-kv-endpoint-login-success-sshuserlogin') and InList(toLower(result), 'success', 'true') |