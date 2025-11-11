# Code Changes for microsoft-evsecurity-json-user-create-success-4720-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'auth_package', 'auth_process', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_user', 'time', 'user', 'user_sid', 'user_type'] |
| edit_regex_field | account_domain |  | ['TargetDomainName\\?"+:\\?"+({dest_domain}({account_domain}[^"\\]+))'] |
| edit_regex_field | account_name |  | ['TargetUserName\\?"+:\\?"+({dest_user}({account_name}[^"\\]+))'] |
| edit_regex_field | domain |  | ['SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\]+)))\\?"'] |
| edit_regex_field | src_host_windows |  | ['WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| edit_regex_field | user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| added_regex_field | dest_domain |  | ['TargetDomainName\\?"+:\\?"+({dest_domain}({account_domain}[^"\\]+))'] |
| added_regex_field | dest_user |  | ['TargetUserName\\?"+:\\?"+({dest_user}({account_name}[^"\\]+))'] |
| added_regex_field | src_domain |  | ['SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\]+)))\\?"'] |
| added_regex_field | src_host |  | ['WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| added_regex_field | src_user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| removed_attribute | DupFields |  | N/A |