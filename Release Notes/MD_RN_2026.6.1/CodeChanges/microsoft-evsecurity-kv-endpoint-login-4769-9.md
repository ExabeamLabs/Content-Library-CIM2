# Code Changes for microsoft-evsecurity-kv-endpoint-login-4769-9 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['sntdom=({domain}[^\s]+)', 'suser=(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['suser=(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_upn |  | ['suser=(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |