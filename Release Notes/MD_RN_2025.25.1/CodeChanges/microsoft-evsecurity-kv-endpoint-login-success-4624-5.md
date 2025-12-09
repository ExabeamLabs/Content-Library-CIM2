# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4624-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['endpoint-login:success', 'endpoint-unlock:success'] |
| edit_attribute | legacy_activity_type |  | ['batch-logon', 'local-logon', 'remote-access', 'remote-logon', 'service-logon', 'workstation-unlocked'] |