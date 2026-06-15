# Code Changes for liquidfiles-l-json-user-password-reset-success-password (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"user_email":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', '"username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_domain |  | ['"user_email":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |