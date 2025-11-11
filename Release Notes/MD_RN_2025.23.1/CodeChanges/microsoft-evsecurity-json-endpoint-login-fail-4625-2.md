# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4625-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | domain |  | ['TargetDomainName\\?"+:\\?"(?:-|\.|NT AUTHORITY| |({dest_domain}({domain}[^\s\\]+?)))\\?"', 'TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"'] |
| edit_regex_field | host |  | ['(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | result_code |  | ['Status\\?"+:\\?"+({result_code}[^\\]+)\\?"', 'SubStatus\\?"+:\\?"+({failure_code}({result_code}[^\\]+))\\?'] |
| edit_regex_field | user |  | ['TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"'] |
| edit_regex_field | user_sid |  | ['SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"', 'TargetUserSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\]+))\\?"'] |
| edit_regex_field | user_upn |  | ['TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"'] |
| added_regex_field | dest_domain |  | ['TargetDomainName\\?"+:\\?"(?:-|\.|NT AUTHORITY| |({dest_domain}({domain}[^\s\\]+?)))\\?"', 'TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"'] |
| added_regex_field | dest_host |  | ['(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_user |  | ['TargetUserName\\?"+:\\?"+(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+)))?)|({user_upn}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?)))\\?"'] |
| added_regex_field | dest_user_sid |  | ['TargetUserSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\]+))\\?"'] |
| added_regex_field | failure_code |  | ['SubStatus\\?"+:\\?"+({failure_code}({result_code}[^\\]+))\\?'] |
| removed_attribute | DupFields |  | N/A |