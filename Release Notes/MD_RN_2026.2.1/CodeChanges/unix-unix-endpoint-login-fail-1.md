# Code Changes for unix-unix-endpoint-login-fail-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'unix-unix-kv-endpoint-login-sshdauth','unix-unix-kv-endpoint-login-userstart', 'unix-unix-kv-endpoint-login-success-sshuserlogin') and !InList(toLower(result), 'success', 'true') |