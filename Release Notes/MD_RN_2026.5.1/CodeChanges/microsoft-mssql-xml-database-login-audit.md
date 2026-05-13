# Code Changes for microsoft-mssql-xml-database-login-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'db_name', 'dest_host', 'domain', 'email_address', 'event_code', 'host', 'result', 'run_level', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | domain |  | ['<Message>.+?user\s\'((({domain}[^\\\']+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\''] |
| edit_regex_field | email_address |  | ['<Message>.+?user\s\'((({domain}[^\\\']+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\''] |
| edit_regex_field | user |  | ['<Message>.+?user\s\'((({domain}[^\\\']+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\''] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |