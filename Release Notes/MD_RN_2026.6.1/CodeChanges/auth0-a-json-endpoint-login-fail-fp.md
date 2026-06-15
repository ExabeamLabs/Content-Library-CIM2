# Code Changes for auth0-a-json-endpoint-login-fail-fp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_regex="user_name":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))'] |
| edit_regex_field | email_domain |  | ['exa_regex="user_name":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_regex="user_name":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))', 'exa_regex="user_name":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,\.]+))?)$'] |