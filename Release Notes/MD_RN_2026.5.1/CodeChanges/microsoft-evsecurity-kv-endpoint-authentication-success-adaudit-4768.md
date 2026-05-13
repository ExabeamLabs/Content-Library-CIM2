# Code Changes for microsoft-evsecurity-kv-endpoint-authentication-success-adaudit-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_upn |  | ['New Logon:[^"]*?Account Name(:|=)\s*(-|SYSTEM|(({user_upn}[^\s\]@]+@[^\s\]@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'USERNAME\s*=\s*({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)\s*\]'] |