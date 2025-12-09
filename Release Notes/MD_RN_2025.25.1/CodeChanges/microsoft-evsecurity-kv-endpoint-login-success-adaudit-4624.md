# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-adaudit-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['endpoint-login:success', 'endpoint-unlock:success'] |
| edit_attribute | legacy_activity_type |  | ['batch-logon', 'local-logon', 'remote-access', 'remote-logon', 'service-logon', 'workstation-unlocked'] |
| edit_attribute | legacy_product |  | ['DC', 'Windows'] |