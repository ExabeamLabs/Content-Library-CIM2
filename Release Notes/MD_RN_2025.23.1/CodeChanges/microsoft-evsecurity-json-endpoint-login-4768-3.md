# Code Changes for microsoft-evsecurity-json-endpoint-login-4768-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'action', 'activity_id', 'app', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'key_name', 'key_type', 'login_id', 'login_type', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'result_code', 'sid_history', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['"TargetUserName"+:"+({dest_user}[^"]+)', 'TargetUserName\\?"+:\\?"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| edit_regex_field | domain |  | ['TargetDomainName\\?"+:\\?"(?:-|({dest_domain}({domain}[^\s\\]+?)))\\?"'] |
| edit_regex_field | result_code |  | ['Status\\?"+:\\?"({failure_code}({result_code}[\w\-]+))\\?"'] |
| edit_regex_field | user |  | ['"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'TargetUserName\\?"+:\\?"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| edit_regex_field | user_sid |  | ['"+SubjectUserSid"+:"+({user_sid}[^"]+)', '"TargetUserSid"+:"+({user_sid}[^"]+)', 'TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"'] |
| added_regex_field | dest_domain |  | ['TargetDomainName\\?"+:\\?"(?:-|({dest_domain}({domain}[^\s\\]+?)))\\?"'] |
| added_regex_field | dest_user_sid |  | ['TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"'] |
| added_regex_field | failure_code |  | ['Status\\?"+:\\?"({failure_code}({result_code}[\w\-]+))\\?"'] |
| removed_attribute | DupFields |  | N/A |