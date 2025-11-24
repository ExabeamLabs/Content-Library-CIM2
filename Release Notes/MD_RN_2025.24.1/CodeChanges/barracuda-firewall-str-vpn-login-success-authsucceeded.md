# Code Changes for barracuda-firewall-str-vpn-login-success-authsucceeded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'email_address', 'event_name', 'host', 'result', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | email_address |  | ["Login\s+'(({email_address}[^'@\(]+@[^'\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'", '\W(login|user)=(({email_address}[^@\(]+@[^\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)'] |
| edit_regex_field | src_ip |  | ['\W(login|user)=(({email_address}[^@\(]+@[^\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)'] |
| edit_regex_field | src_port |  | ['\W(login|user)=(({email_address}[^@\(]+@[^\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)'] |
| edit_regex_field | user |  | ["Login\s+'(({email_address}[^'@\(]+@[^'\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'", '\W(login|user)=(({email_address}[^@\(]+@[^\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)'] |
| added_regex_field | account |  | ["Login\s+'(({email_address}[^'@\(]+@[^'\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'", '\W(login|user)=(({email_address}[^@\(]+@[^\(@]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)'] |
| removed_attribute | DupFields |  | N/A |