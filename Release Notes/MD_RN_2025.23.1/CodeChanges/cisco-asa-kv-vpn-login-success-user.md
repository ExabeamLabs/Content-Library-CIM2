# Code Changes for cisco-asa-kv-vpn-login-success-user (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'email_address', 'src_host', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | email_address |  | ['DAP: User (({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['DAP: User (({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | account |  | ['DAP: User (({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |