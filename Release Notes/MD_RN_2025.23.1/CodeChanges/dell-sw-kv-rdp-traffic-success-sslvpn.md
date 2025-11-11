# Code Changes for dell-sw-kv-rdp-traffic-success-sslvpn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'bytes', 'bytes_in', 'bytes_out', 'dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'protocol', 'realm', 'session_duration', 'src_host', 'src_interface', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | email_address |  | ['\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\susr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"'] |
| edit_regex_field | user |  | ['\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\susr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"'] |
| added_regex_field | account |  | ['\suser="\s*(({email_address}[^@"]+@[^\\\s"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\susr="\s*(({email_address}[^@"]+@[^\\\s"]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"'] |
| removed_attribute | DupFields |  | N/A |