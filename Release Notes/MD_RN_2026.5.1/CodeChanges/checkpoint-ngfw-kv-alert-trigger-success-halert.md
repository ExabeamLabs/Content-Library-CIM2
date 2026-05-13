# Code Changes for checkpoint-ngfw-kv-alert-trigger-success-halert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\W(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)'] |
| edit_regex_field | full_name |  | ['\W(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', '\W(user|src_user_name|dst_user_name)"?:"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | user |  | ['\W(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)', '\W(user|src_user_name|dst_user_name)"?:"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |