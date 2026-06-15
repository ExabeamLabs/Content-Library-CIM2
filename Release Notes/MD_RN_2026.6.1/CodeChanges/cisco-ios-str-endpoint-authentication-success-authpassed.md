# Code Changes for cisco-ios-str-endpoint-authentication-success-authpassed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['User \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | email_domain |  | ['User \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | user |  | ['User \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | user_id |  | ['User \'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |