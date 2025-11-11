# Code Changes for cisco-asa-kv-radius-traffic-success-113004-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'domain', 'email_address', 'event_code', 'event_name', 'first_name', 'host', 'last_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | domain |  | ['user\s*=\s*((cn=({src_host}[^>,\s]+)(,[^>]+?dc=({domain}[^>,]+))?)|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))', 'user\s*=\s*(({domain}[^\\s]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_address |  | ['user\s*=\s*((cn=({src_host}[^>,\s]+)(,[^>]+?dc=({domain}[^>,]+))?)|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))', 'user\s*=\s*(({domain}[^\\s]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['user\s*=\s*(({domain}[^\\s]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | account |  | ['user\s*=\s*(({domain}[^\\s]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |