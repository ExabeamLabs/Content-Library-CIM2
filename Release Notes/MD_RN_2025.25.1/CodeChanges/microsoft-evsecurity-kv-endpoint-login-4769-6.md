# Code Changes for microsoft-evsecurity-kv-endpoint-login-4769-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['endpoint-authentication:fail', 'endpoint-authentication:success'] |
| edit_attribute | legacy_activity_type |  | ['authentication-failed', 'kerberos-logon'] |