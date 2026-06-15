# Code Changes for cisco-duo-cef-app-login-destservicenameduo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"email":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', '"object":\s*"(({email_address}[^"@\s]+@[^"\s@]+)|({object}[^"]+))', '"username"+:"+(?!AD Sync:|AD User Sync:)(({email_address}[^"\s@]+@({email_domain}[^"\s@]+))|({full_name}[^\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_domain |  | ['"email":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', '"username"+:"+(?!AD Sync:|AD User Sync:)(({email_address}[^"\s@]+@({email_domain}[^"\s@]+))|({full_name}[^\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |