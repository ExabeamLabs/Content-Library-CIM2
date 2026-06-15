# Code Changes for microsoft-azuresc-sk4-alert-trigger-success-asc (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"userPrincipalName":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)\\?"', 'domainName":"(null|({domain}[^,]+?))\s*"'] |
| edit_regex_field | email_address |  | ['"userPrincipalName":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)\\?"', '"userPrincipalName":"(null|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({full_name}[^\s"]+\s+[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | full_name |  | ['"userPrincipalName":"(null|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({full_name}[^\s"]+\s+[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | user |  | ['"userPrincipalName":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)\\?"', '"userPrincipalName":"(null|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({full_name}[^\s"]+\s+[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |