# Code Changes for juniper-ps-str-vpn-login-success-connected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | domain |  | ['\s+-\s+\[[^\]]+\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s]+)|(({domain}[^\(]+)\\)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)'] |
| edit_regex_field | email_address |  | ['\s+-\s+\[[^\]]+\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s]+)|(({domain}[^\(]+)\\)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)'] |
| edit_regex_field | realm |  | ['\s+-\s+\[[^\]]+\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s]+)|(({domain}[^\(]+)\\)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)'] |
| edit_regex_field | user |  | ['\s+-\s+\[[^\]]+\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s]+)|(({domain}[^\(]+)\\)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)'] |
| added_regex_field | account |  | ['\s+-\s+\[[^\]]+\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s]+)|(({domain}[^\(]+)\\)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)'] |
| removed_attribute | DupFields |  | N/A |