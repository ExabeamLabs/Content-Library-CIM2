# Code Changes for zscaler-internetaccess-app-login-success (Event Builder)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'zscaler-ia-json-security-activity-success') && toLower(action), 'login pass' | InList(type, 'zscaler-ia-json-security-activity-success') && toLower(action) = 'login pass' |