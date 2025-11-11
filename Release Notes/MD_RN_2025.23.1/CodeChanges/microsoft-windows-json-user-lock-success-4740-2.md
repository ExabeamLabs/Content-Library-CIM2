# Code Changes for microsoft-windows-json-user-lock-success-4740-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_domain |  | ['SubjectDomainName\\?"+:\\?"({domain}({src_domain}[^\\"]+))\\?"', 'SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^\\]+))\\?"'] |
| edit_regex_field | user |  | ['TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"', 'TargetUserName\\?"+:\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"'] |
| edit_regex_field | user_sid |  | ['SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"', 'TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"', 'TargetSid\\?"+:\\?"({user_sid}[^\\]+)\\?"'] |
| added_regex_field | dest_user |  | ['TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"'] |
| added_regex_field | dest_user_sid |  | ['SubjectUserSid\\?"+:\\?"+({dest_user_sid}[^\\]+)\\?"', 'TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"'] |
| added_regex_field | domain |  | ['SubjectDomainName\\?"+:\\?"({domain}({src_domain}[^\\"]+))\\?"', 'SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?"', 'TargetDomainName\\?"+:\\?"({domain}[^\s\\]+)\\?"'] |
| removed_attribute | DupFields |  | N/A |