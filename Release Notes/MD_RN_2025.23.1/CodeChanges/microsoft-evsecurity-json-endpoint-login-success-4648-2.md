# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4648-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'account_login_guid', 'auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_login_guid', 'user_sid'] |
| edit_regex_field | dest_domain |  | ['TargetDomainName\\?"+:\\?"(\.|({account_domain}({dest_domain}[^\\"]+)))\\?"'] |
| edit_regex_field | dest_user |  | ['TargetUserName\\?"+:\\?"(LOCAL SYSTEM|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| edit_regex_field | domain |  | ['SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\"]+)))\\?"'] |
| edit_regex_field | src_host_windows |  | ['WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| edit_regex_field | user |  | ['"user":\{[^\}]*?"name":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| added_regex_field | account |  | ['TargetUserName\\?"+:\\?"(LOCAL SYSTEM|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| added_regex_field | account_domain |  | ['TargetDomainName\\?"+:\\?"(\.|({account_domain}({dest_domain}[^\\"]+)))\\?"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\"]+)))\\?"'] |
| added_regex_field | src_host |  | ['WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| added_regex_field | src_user |  | ['"user":\{[^\}]*?"name":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| removed_attribute | DupFields |  | N/A |