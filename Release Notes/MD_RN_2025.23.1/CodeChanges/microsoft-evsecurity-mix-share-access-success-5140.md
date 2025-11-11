# Code Changes for microsoft-evsecurity-mix-share-access-success-5140 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'file_path', 'file_type', 'host', 'login_id', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | d_name |  | ['Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({file_path}({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?))))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:'] |
| edit_regex_field | d_parent |  | ['Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({file_path}({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?))))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:'] |
| edit_regex_field | domain |  | ['Account Domain:\s*((\\)*(\\r|\\t|\\n))*({domain}\S+?)((\\)*(\\r|\\t|\\n))*\s*Logon ID:', 'SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\]+)))\\?"'] |
| edit_regex_field | share_path |  | ['Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({file_path}({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?))))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:'] |
| edit_regex_field | src_domain |  | ['SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\]+)))\\?"'] |
| edit_regex_field | src_user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| edit_regex_field | user |  | ['Account Name:\s*((\\)*(\\r|\\t|\\n))*({user}[\w\.\-\!\#\^\~]{1,40}\$?)((\\)*(\\r|\\t|\\n))*\s*Account Domain:', 'SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| added_regex_field | file_path |  | ['Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({file_path}({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?))))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:'] |
| removed_attribute | DupFields |  | N/A |