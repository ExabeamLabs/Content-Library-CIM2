# Code Changes for unix-unix-sk4-endpoint-login-success-linuxsyslogevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth |  | ['Accepted\s({auth}\S+)\sfor\s(({domain}[^\\"]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |
| edit_regex_field | domain |  | ['Accepted\s({auth}\S+)\sfor\s(({domain}[^\\"]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |
| edit_regex_field | email_address |  | ['Accepted\s({auth}\S+)\sfor\s(({domain}[^\\"]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |
| edit_regex_field | user |  | ['Accepted\s({auth}\S+)\sfor\s(({domain}[^\\"]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |