# Code Changes for microsoft-evsecurity-sk4-user-create-success-usercreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"UserPrincipalName":"({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+))?)"'] |
| edit_regex_field | user_upn |  | ['"UserPrincipalName":"({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+))?)"'] |