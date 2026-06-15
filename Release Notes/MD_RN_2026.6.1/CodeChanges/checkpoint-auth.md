# Code Changes for checkpoint-auth (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', '\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | full_name |  | ['\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | user |  | ['\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"', '\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', '\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)'] |