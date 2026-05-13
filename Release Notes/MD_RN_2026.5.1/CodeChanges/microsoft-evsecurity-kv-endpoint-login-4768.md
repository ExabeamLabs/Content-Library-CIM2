# Code Changes for microsoft-evsecurity-kv-endpoint-login-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['"UserName":"(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'Account Name:\s*(({full_name}[^:]+?\s[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Supplied Realm Name', '\sAccount Name:\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_upn |  | ['"UserName":"(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '\sAccount Name:\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |