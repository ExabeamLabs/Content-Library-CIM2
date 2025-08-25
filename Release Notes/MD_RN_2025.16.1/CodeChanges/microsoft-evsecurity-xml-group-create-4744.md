# Code Changes for microsoft-evsecurity-xml-group-create-4744 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<Data Name=', '<EventID>4744</EventID>', 'Microsoft-Windows-Security-Auditing', 'TargetUserName'] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)</Data>'] |
| edit_regex_field | group_domain |  | ['<Data Name=(\'|")TargetDomainName(\'|")>({group_domain}[^<>]+?)</Data>'] |
| edit_regex_field | group_id |  | ['<Data Name=(\'|")TargetSid(\'|")>({group_id}[^<>]+?)<\/Data>'] |
| edit_regex_field | group_name |  | ['<Data Name=(\'|")TargetUserName(\'|")>({group_name}[^<>]+?)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)</Data>'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)'] |