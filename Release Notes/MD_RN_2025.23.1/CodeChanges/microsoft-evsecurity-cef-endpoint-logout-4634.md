# Code Changes for microsoft-evsecurity-cef-endpoint-logout-4634 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_domain |  | ['<Data Name=(\'|")TargetDomainName(\'|")>({domain}({dest_domain}[^<]+))<'] |
| edit_regex_field | dest_login_id |  | ['<Data Name\\=(\'|")TargetLogonId(\'|")>({login_id}({dest_login_id}[^<]+))<'] |
| edit_regex_field | dest_user |  | ['<Data Name=(\'|")TargetUserName(\'|")>(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| edit_regex_field | dest_user_sid |  | ['<Data Name\\=(\'|")TargetUserSid(\'|")>({user_sid}({dest_user_sid}[^<]+))<'] |
| edit_regex_field | login_id |  | ['<Data Name\\=(\'|")SubjectLogonId(\'|")>(-|({login_id}[^<>]+))<', '<Data Name\\=(\'|")TargetLogonId(\'|")>({login_id}({dest_login_id}[^<]+))<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\=(\'|")SubjectUserSid(\'|")>(-|({user_sid}[^<>]+))<', '<Data Name\\=(\'|")TargetUserSid(\'|")>({user_sid}({dest_user_sid}[^<]+))<'] |
| added_regex_field | domain |  | ['<Data Name=(\'|")TargetDomainName(\'|")>({domain}({dest_domain}[^<]+))<'] |
| added_regex_field | user |  | ['<Data Name=(\'|")TargetUserName(\'|")>(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |