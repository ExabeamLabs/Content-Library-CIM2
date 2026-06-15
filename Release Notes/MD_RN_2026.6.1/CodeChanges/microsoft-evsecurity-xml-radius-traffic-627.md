# Code Changes for microsoft-evsecurity-xml-radius-traffic-627 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['Account Name:\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain', 'Account Name:\s*({user_type}[^\s:]+?)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\.[^:\.\s]+?)*\s*Account Domain'] |
| edit_regex_field | user_upn |  | ['Account Name:\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain'] |