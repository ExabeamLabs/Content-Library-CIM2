# Code Changes for azure-azuread-json-user-password-modify-success-selfservice (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_attribute | activity_type | ['user-password-modify:success'] | ['app-activity:success', 'user-password-modify:fail', 'user-password-modify:success'] |
| edit_attribute | legacy_activity_type | ['account-password-change'] | ['account-password-change', 'account-password-change-failed', 'app-activity'] |