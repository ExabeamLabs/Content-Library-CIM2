# Code Changes for microsoft-evsecurity-json-user-switch-success-4648 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | ['"TargetServerName":', '4648', 'A logon was attempted using explicit credentials', 'Microsoft-Windows-Security-Auditing'] | ['"TargetServerName":', '4648'] |
| edit_attribute | activity_type | ['endpoint-login:success'] | ['endpoint-login:success', 'user-switch:success'] |