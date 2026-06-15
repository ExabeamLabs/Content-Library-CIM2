# Code Changes for fortinet-firewall-kv-network-traffic-notice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\Wuser="\s*((?:host\/({src_host}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)\s*"'] |
| edit_regex_field | email_address |  | ['\Wuser="\s*((?:host\/({src_host}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)\s*"'] |
| edit_regex_field | src_host |  | ['\Wuser="\s*((?:host\/({src_host}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)\s*"', '\ssrcname=\"*({src_host}[\w\-.]+)\"*'] |
| edit_regex_field | user |  | ['\Wuser="\s*((?:host\/({src_host}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)\s*"'] |