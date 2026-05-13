# Code Changes for unix-unix-kv-endpoint-login-success-httpd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\[(-|(({domain}[^\\\]]+)\\{1,25})?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\]:\s*({event_name}Login_Allowed)'] |
| edit_regex_field | email_address |  | ['\[(-|(({domain}[^\\\]]+)\\{1,25})?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\]:\s*({event_name}Login_Allowed)'] |
| edit_regex_field | event_name |  | ['\[(-|(({domain}[^\\\]]+)\\{1,25})?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\]:\s*({event_name}Login_Allowed)'] |
| edit_regex_field | user |  | ['\[(-|(({domain}[^\\\]]+)\\{1,25})?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\]:\s*({event_name}Login_Allowed)'] |