# Code Changes for microsoft-evsecurity-xml-app-activity-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'opcode', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_domain |  | ['Data Name(\\)?=(\'|")TargetDomainName(\'|")>({domain}({dest_domain}[^<]+))'] |
| edit_regex_field | dest_login_id |  | ['Data Name(\\)?=(\'|")TargetLogonId(\'|")>({login_id}({dest_login_id}[^<]+))'] |
| edit_regex_field | dest_user |  | ['Data Name(\\)?=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | dest_user_sid |  | ['Data Name(\\)?=(\'|")TargetUserSid(\'|")>({user_sid}({dest_user_sid}[^<]+))'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'"]+)(\'|")\/>', 'Data Name(\\)?=(\'|")TargetUserSid(\'|")>({user_sid}({dest_user_sid}[^<]+))'] |
| added_regex_field | domain |  | ['Data Name(\\)?=(\'|")TargetDomainName(\'|")>({domain}({dest_domain}[^<]+))'] |
| added_regex_field | login_id |  | ['Data Name(\\)?=(\'|")TargetLogonId(\'|")>({login_id}({dest_login_id}[^<]+))'] |
| added_regex_field | user |  | ['Data Name(\\)?=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| removed_attribute | DupFields |  | N/A |