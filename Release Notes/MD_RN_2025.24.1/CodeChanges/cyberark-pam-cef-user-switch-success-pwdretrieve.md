# Code Changes for cyberark-pam-cef-user-switch-success-pwdretrieve (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'additional_info', 'dest_domain', 'dest_email_address', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'device_type', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'operation', 'safe_value', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_user |  | ['\sduser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_domain}[^\\=]+?)(\\)+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | domain |  | ['\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | event_code |  | ['CEF:\s*\d+\|([^\|]+\|){3}({event_code}[^\|]+)'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\dZ? ({host}[\w\-.]+) CEF:', '\sdvc=({host}\S+?)(\s+\w+=|\s*$)', '\sdvchost=({host}\S+?)(\s+\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| added_regex_field | dest_domain |  | ['\sduser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_domain}[^\\=]+?)(\\)+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| added_regex_field | dest_email_address |  | ['\sduser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_domain}[^\\=]+?)(\\)+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| added_regex_field | email_address |  | ['\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |