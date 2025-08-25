# Code Changes for microsoft-windows-cef-endpoint-login-device (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_attribute | activity_type | ['endpoint-login:fail', 'endpoint-login:success'] | ['endpoint-login:fail', 'endpoint-login:success', 'endpoint-notification:success'] |
| edit_attribute | legacy_activity_type | ['authentication-failed', 'authentication-successful'] | ['app-activity', 'authentication-failed', 'authentication-successful'] |