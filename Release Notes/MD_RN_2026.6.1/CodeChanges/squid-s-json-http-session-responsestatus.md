# Code Changes for squid-s-json-http-session-responsestatus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['http_username":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | user |  | ['http_username":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |