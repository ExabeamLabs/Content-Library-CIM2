# Code Changes for unix-unix-str-endpoint-login-fail-check (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['password check failed for user \(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)'] |
| edit_regex_field | user |  | ['password check failed for user \(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)'] |