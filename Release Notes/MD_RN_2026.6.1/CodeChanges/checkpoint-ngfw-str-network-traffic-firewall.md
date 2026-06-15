# Code Changes for checkpoint-ngfw-str-network-traffic-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\W(user|src_user_name|dst_user_name):\"+(?:[^_\"\s]+_)?(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\"', '\Wdst_user_name:\"+(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[^\"@]+@[^\"@]+))\s*\"', '\Wsrc_user_name:\"+(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[^\"@\(\)]+@[\(\)^\"@]+))\s*\"', '\Wuser:\"+({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*\"'] |
| edit_regex_field | email_domain |  | ['\Wuser:\"+({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*\"'] |