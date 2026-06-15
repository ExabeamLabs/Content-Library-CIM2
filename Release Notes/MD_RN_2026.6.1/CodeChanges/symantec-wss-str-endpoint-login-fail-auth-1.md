# Code Changes for symantec-wss-str-endpoint-login-fail-auth-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | [' user \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\' \(domain (\(null\)|({domain}[^\)]+))\)'] |
| edit_regex_field | email_address |  | [' user \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\' \(domain (\(null\)|({domain}[^\)]+))\)'] |
| edit_regex_field | user |  | [' user \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\' \(domain (\(null\)|({domain}[^\)]+))\)'] |