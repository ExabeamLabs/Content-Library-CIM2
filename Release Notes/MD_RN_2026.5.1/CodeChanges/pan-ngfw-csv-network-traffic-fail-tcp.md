# Code Changes for pan-ngfw-csv-network-traffic-fail-tcp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | [',TRAFFIC,([^,]*,){8}\s*(|\d|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?:({domain}({src_domain}[^\s,\\]+))\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))),'] |
| edit_regex_field | email_address |  | [',TRAFFIC,([^,]*,){8}\s*(|\d|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?:({domain}({src_domain}[^\s,\\]+))\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))),'] |
| edit_regex_field | src_domain |  | [',TRAFFIC,([^,]*,){8}\s*(|\d|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?:({domain}({src_domain}[^\s,\\]+))\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))),'] |
| edit_regex_field | src_user |  | [',TRAFFIC,([^,]*,){8}\s*(|\d|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?:({domain}({src_domain}[^\s,\\]+))\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))),'] |
| edit_regex_field | user |  | [',TRAFFIC,([^,]*,){8}\s*(|\d|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?:({domain}({src_domain}[^\s,\\]+))\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))),'] |