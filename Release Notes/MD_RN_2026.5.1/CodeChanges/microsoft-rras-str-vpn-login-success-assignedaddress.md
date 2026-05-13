# Code Changes for microsoft-rras-str-vpn-login-success-assignedaddress (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'email_address', 'email_domain', 'session_id', 'src_translated_ip', 'user'] |
| edit_regex_field | email_address |  | [':\s*The user (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+connected on port'] |
| edit_regex_field | email_domain |  | [':\s*The user (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+connected on port'] |
| edit_regex_field | user |  | [':\s*The user (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+connected on port'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |