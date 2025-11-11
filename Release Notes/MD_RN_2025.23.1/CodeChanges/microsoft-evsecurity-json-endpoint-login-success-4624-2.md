# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4624-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['TargetDomainName\\?"+:\\?"({dest_domain}({domain}[^\s"\\]+))\\?"'] |
| edit_regex_field | host |  | ['(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | src_host_windows |  | ['WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| edit_regex_field | user |  | ['TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"'] |
| edit_regex_field | user_sid |  | ['SubjectUserSid\\?"+:\\?"+({dest_user_sid}({user_sid}[^\\"]+))\\?"', 'TargetUserSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"'] |
| added_regex_field | dest_domain |  | ['TargetDomainName\\?"+:\\?"({dest_domain}({domain}[^\s"\\]+))\\?"'] |
| added_regex_field | dest_host |  | ['(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_user |  | ['TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"'] |
| added_regex_field | dest_user_sid |  | ['SubjectUserSid\\?"+:\\?"+({dest_user_sid}({user_sid}[^\\"]+))\\?"', 'TargetUserSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"'] |
| added_regex_field | src_host |  | ['WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| removed_attribute | DupFields |  | N/A |