# Code Changes for microsoft-windows-share-access-fail-3 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-kv-endpoint-authentication-fail-551', 'microsoft-evsecurity-kv-share-access-fail-1009', 'microsoft-evsecurity-kv-share-access-fail-smbserver') and !InList(ToLower(result), 'granted', 'success', 'audit success') |