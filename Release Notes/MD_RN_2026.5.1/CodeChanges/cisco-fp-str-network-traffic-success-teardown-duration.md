# Code Changes for cisco-fp-str-network-traffic-success-teardown-duration (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(({email_address}[^@\)]+@[^\.\)]+\.[^,\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | email_address |  | ['%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(({email_address}[^@\)]+@[^\.\)]+\.[^,\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', '\sduration\s+({duration}\S+)\s+bytes\s+({bytes}\d+)(\s+({result_reason}[^\(]+[^\(\s]))?(\s+\((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))?'] |
| edit_regex_field | user |  | ['%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(({email_address}[^@\)]+@[^\.\)]+\.[^,\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', '\sduration\s+({duration}\S+)\s+bytes\s+({bytes}\d+)(\s+({result_reason}[^\(]+[^\(\s]))?(\s+\((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))?'] |