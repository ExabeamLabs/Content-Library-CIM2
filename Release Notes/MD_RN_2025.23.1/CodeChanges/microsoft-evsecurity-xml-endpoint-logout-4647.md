# Code Changes for microsoft-evsecurity-xml-endpoint-logout-4647 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'result', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))<\/Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")TargetLogonId(\'|")>({dest_login_id}({login_id}[^<]+))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<\/Data>'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))<\/Data>'] |
| added_regex_field | dest_login_id |  | ['<Data Name\\*=(\'|")TargetLogonId(\'|")>({dest_login_id}({login_id}[^<]+))<\/Data>'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>'] |
| added_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |