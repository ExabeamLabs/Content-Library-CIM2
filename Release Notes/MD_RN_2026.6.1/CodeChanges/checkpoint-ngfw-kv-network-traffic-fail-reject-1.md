# Code Changes for checkpoint-ngfw-kv-network-traffic-fail-reject-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | full_name |  | ['(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | user |  | ['(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |