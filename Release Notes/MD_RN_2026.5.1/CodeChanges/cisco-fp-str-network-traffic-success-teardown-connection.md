# Code Changes for cisco-fp-str-network-traffic-success-teardown-connection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(?:({email_address}[^@\\\/)]+@[^\\\/)]+\.[^,\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | email_address |  | ['%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(?:({email_address}[^@\\\/)]+@[^\\\/)]+\.[^,\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | user |  | ['%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(?:({email_address}[^@\\\/)]+@[^\\\/)]+\.[^,\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |