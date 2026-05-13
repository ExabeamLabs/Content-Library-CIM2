# Code Changes for hp-arubawc-kv-endpoint-login-fail-authfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['username=(host\/({src_host}[\w\-.]+)|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\)?({=user}[^\s]+))\s+\w+='] |
| edit_regex_field | email_address |  | ['username=(host\/({src_host}[\w\-.]+)|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\)?({=user}[^\s]+))\s+\w+='] |
| edit_regex_field | src_host |  | ['username=(host\/({src_host}[\w\-.]+)|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\)?({=user}[^\s]+))\s+\w+='] |
| edit_regex_field | user |  | ['username=(host\/({src_host}[\w\-.]+)|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\)?({=user}[^\s]+))\s+\w+='] |