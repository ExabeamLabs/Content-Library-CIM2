# Code Changes for microsoft-evsecurity-kv-ds-object-activity-success-4662-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['Account Domain:(\\t|\\r|\\n)*\s*(|({domain}[^:]+?))(\\t|\\r|\\n)*\s*Logon ID:', 'Account Name:(\\r|\\n|\\t|\s)*(-|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\r|\\n|\\t|\s)*.+?Account Domain:'] |
| edit_regex_field | user |  | ['Account Name:(\\r|\\n|\\t|\s)*(-|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\r|\\n|\\t|\s)*.+?Account Domain:'] |
| edit_regex_field | user_upn |  | ['Account Name:(\\r|\\n|\\t|\s)*(-|({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+)?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\r|\\n|\\t|\s)*.+?Account Domain:'] |