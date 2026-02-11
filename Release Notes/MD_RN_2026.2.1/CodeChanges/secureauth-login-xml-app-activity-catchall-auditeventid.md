# Code Changes for secureauth-login-xml-app-activity-catchall-auditeventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'email_address', 'event_id', 'full_name', 'host', 'priority', 'src_ip', 'src_port', 'user', 'user_agent'] |
| edit_regex_field | user |  | ['<UserID>(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<\/UserID>'] |
| removed_regex_field | user_id |  | [] |
| added_regex_field | email_address |  | ['<UserID>(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<\/UserID>'] |
| added_regex_field | full_name |  | ['<UserID>(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<\/UserID>'] |