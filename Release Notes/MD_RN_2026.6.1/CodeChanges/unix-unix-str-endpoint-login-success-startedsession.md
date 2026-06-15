# Code Changes for unix-unix-str-endpoint-login-success-startedsession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['of user (({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}?\$?))\.?"*$'] |
| edit_regex_field | user |  | ['of user (({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}?\$?))\.?"*$'] |