# Code Changes for juniper-ps-str-vpn-login-success-passed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'email_address', 'host', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | email_address |  | ["for user '(({email_address}[^@\s']+@[^\.\s']+\.[^\s']+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"] |
| edit_regex_field | user |  | ['(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)?\s+PulseSecure:((\s\S+){3}\s|\s+)({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)\s+(\S+\s+){3}\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\((|unknown|({realm}[^)]+))\)', "for user '(({email_address}[^@\s']+@[^\.\s']+\.[^\s']+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"] |
| added_regex_field | account |  | ["for user '(({email_address}[^@\s']+@[^\.\s']+\.[^\s']+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"] |
| removed_attribute | DupFields |  | N/A |