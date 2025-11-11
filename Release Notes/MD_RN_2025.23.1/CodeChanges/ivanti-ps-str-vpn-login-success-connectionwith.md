# Code Changes for ivanti-ps-str-vpn-login-success-connectionwith (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'event_name', 'host', 'realm', 'src_ip', 'time', 'user', 'vpn_client_type'] |
| edit_regex_field | realm |  | ['PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)\)'] |
| edit_regex_field | src_ip |  | ['PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)\)'] |
| edit_regex_field | time |  | ['PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)\)'] |
| edit_regex_field | user |  | ['PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)\)'] |
| added_regex_field | account |  | ['PulseSecure:.+?-\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*-\s*[^\s]+\s*-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)\)'] |
| removed_attribute | DupFields |  | N/A |