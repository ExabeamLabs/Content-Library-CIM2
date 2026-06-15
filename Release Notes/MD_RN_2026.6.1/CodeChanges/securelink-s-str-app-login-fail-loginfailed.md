# Code Changes for securelink-s-str-app-login-fail-loginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['Key:\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?)),'] |
| edit_regex_field | email_domain |  | ['Key:\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?)),'] |
| edit_regex_field | user |  | ['Key:\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?)),', 'User:\s*(SYSLOG|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?))'] |