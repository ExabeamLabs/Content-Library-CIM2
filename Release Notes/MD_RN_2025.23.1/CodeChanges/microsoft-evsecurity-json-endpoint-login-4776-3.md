# Code Changes for microsoft-evsecurity-json-endpoint-login-4776-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type_text', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | domain |  | ['TargetUserName\\?"+:\\?"+((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?"'] |
| edit_regex_field | user |  | ['TargetUserName\\?"+:\\?"+((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?"'] |
| edit_regex_field | user_upn |  | ['TargetUserName\\?"+:\\?"+((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?"'] |
| added_regex_field | dest_domain |  | ['TargetUserName\\?"+:\\?"+((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?"'] |
| added_regex_field | dest_user |  | ['TargetUserName\\?"+:\\?"+((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?"'] |
| removed_attribute | DupFields |  | N/A |