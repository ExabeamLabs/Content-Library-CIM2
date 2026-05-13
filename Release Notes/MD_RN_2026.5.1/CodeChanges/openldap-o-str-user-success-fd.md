# Code Changes for openldap-o-str-user-success-fd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['endpoint-activity:fail', 'endpoint-activity:success', 'endpoint-authentication:fail', 'endpoint-authentication:success', 'user-create:fail', 'user-create:success', 'user-delete:fail', 'user-delete:success', 'user-password-modify:fail', 'user-password-modify:success'] |
| edit_attribute | legacy_activity_type |  | ['account-creation', 'account-deleted', 'account-password-change', 'app-activity', 'authentication-failed', 'authentication-successful'] |