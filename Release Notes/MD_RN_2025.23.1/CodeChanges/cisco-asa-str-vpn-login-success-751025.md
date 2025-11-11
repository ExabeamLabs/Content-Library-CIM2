# Code Changes for cisco-asa-str-vpn-login-success-751025 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'email_address', 'event_code', 'host', 'priority', 'realm', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | email_address |  | ['Username:(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))) IKEv2 '] |
| edit_regex_field | user |  | ['Username:(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))) IKEv2 '] |
| added_regex_field | account |  | ['Username:(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))) IKEv2 '] |
| removed_attribute | DupFields |  | N/A |