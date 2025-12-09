# Code Changes for microsoft-evsecurity-cef-endpoint-login-4769-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['endpoint-authentication:fail', 'endpoint-authentication:success'] |
| edit_attribute | legacy_activity_type |  | ['authentication-failed', 'kerberos-logon'] |