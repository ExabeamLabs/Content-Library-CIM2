# Code Changes for microsoft-ad-endpoint-authentication-fail-5 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771') && InList(toLower(result_code), '0x18', '0x12') and not EndsWith(user, '$') |