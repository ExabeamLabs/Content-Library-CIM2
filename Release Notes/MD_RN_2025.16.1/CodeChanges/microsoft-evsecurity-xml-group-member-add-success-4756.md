# Code Changes for microsoft-evsecurity-xml-group-member-add-success-4756 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_domain |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>'] |
| edit_regex_field | account_name |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>'] |
| edit_regex_field | dest_user_sid |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)</Data>'] |
| edit_regex_field | group_domain |  | ['<Data Name(\\)?=(\'|")TargetDomainName(\'|")>(?=\w)({group_domain}[^<]+)</Data>'] |
| edit_regex_field | group_id |  | ['<Data Name(\\)?=(\'|")TargetSid(\'|")>({group_id}[^<]+)</Data>'] |
| edit_regex_field | group_name |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(?=\w)({group_name}[^<]+)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name(\\)?=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)</Data>'] |
| edit_regex_field | member |  | ['<Data Name(\\)?=(\'|")MemberName(\'|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>', '<Data Name=(\'|")MemberName((\'|")>|":")CN\\?=({member}[^>]+)<\/Data>'] |
| edit_regex_field | process_guid |  | ['<System>.*?Guid(\\)?=(\'|")\{({process_guid}[^}]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}\d+)'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_dn |  | ['<Data Name(\\)?=(\'|")MemberName(\'|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>'] |
| edit_regex_field | user_ou |  | ['<Data Name(\\)?=(\'|")MemberName(\'|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name(\\)?=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)</Data>'] |