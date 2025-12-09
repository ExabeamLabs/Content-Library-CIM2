# Code Changes for fortinet-vpn-cef-vpn-login-success-connection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'email_address', 'host', 'realm', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'tz', 'user'] |
| edit_regex_field | email_address |  | ['xauth_?user="+(?:N\/A|({email_address}[^@"]+@[^\."]+\.[^"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | user |  | ['xauth_?user="+(?:N\/A|({email_address}[^@"]+@[^\."]+\.[^"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | account |  | ['xauth_?user="+(?:N\/A|({email_address}[^@"]+@[^\."]+\.[^"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |