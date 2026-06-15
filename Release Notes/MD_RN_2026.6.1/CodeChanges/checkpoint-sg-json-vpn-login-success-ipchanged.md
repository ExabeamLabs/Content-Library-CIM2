# Code Changes for checkpoint-sg-json-vpn-login-success-ipchanged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['user:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | full_name |  | ['user:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | user |  | ['user:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', 'user:+"+CN=(?:[^_]+_)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |