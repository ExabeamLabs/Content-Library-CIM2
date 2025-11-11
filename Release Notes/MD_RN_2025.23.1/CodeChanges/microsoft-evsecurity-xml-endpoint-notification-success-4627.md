# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-4627 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_id', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")TargetLogonId(\'|")>({dest_login_id}({login_id}[^<]+))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<', '<Data Name\\*=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))<'] |
| added_regex_field | dest_login_id |  | ['<Data Name\\*=(\'|")TargetLogonId(\'|")>({dest_login_id}({login_id}[^<]+))<'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| added_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<', '<Data Name\\*=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<'] |
| removed_attribute | DupFields |  | N/A |