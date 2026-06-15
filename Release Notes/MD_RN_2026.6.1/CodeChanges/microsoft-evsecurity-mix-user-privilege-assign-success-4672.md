# Code Changes for microsoft-evsecurity-mix-user-privilege-assign-success-4672 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['Account Name(:|=)\s*(-|SYSTEM|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\\r|\\n|\\t)*[\s;]*Account Domain(:|=)'] |
| edit_regex_field | user_upn |  | ['Account Name(:|=)\s*(-|SYSTEM|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\\r|\\n|\\t)*[\s;]*Account Domain(:|=)'] |