# Code Changes for checkpoint-ngfw-kv-vpn-logout-success-logout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"', '\W(user|src_user_name|dst_user_name):"+.+?\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | user |  | ['\W(user|src_user_name|dst_user_name):"(?:[^_"\s]+_)?(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"', '\W(user|src_user_name|dst_user_name):"+.+?\((({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |