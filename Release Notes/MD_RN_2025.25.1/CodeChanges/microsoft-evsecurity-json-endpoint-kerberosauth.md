# Code Changes for microsoft-evsecurity-json-endpoint-kerberosauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['endpoint-authentication:fail', 'endpoint-authentication:success'] |
| edit_attribute | legacy_activity_type |  | ['authentication-failed', 'kerberos-logon'] |
| edit_attribute | Platform |  | ['Microsoft AD', 'Windows'] |