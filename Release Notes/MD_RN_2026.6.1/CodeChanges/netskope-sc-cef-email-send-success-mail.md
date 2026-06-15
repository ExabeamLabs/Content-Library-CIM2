# Code Changes for netskope-sc-cef-email-send-success-mail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"from_user":"({from_user_at}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"', '"user":\s*"(({from_user_at}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_domain |  | ['"user":\s*"(({from_user_at}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | from_user_at |  | ['"from_user":"({from_user_at}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"', '"user":\s*"(({from_user_at}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"user":\s*"(({from_user_at}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |