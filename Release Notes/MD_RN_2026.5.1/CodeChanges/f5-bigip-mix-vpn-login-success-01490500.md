# Code Changes for f5-bigip-mix-vpn-login-success-01490500 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$.message,exa_regex=\sUsername\s+\'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\''] |
| edit_regex_field | email_address |  | ['exa_json_path=$.message,exa_regex=\sUsername\s+\'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\''] |
| edit_regex_field | user |  | ['exa_json_path=$.message,exa_regex=\sUsername\s+\'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\''] |