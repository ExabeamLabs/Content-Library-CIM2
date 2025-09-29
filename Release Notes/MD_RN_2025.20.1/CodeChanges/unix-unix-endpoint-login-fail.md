# Code Changes for unix-unix-endpoint-login-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'unix-unix-kv-endpoint-login-userlogin','unix-unix-kv-endpoint-login-userstart','unix-unix-kv-endpoint-login-success-userauth','unix-unix-kv-endpoint-login-success-userauth-1') and exists(event_name) and InList(toLower(event_name), 'user_auth', 'user_start','user_login') and !InList(toLower(result), 'success') and exists(dest_host) |