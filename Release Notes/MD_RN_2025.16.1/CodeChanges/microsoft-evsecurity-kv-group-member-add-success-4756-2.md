# Code Changes for microsoft-evsecurity-kv-group-member-add-success-4756-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_domain |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>'] |
| edit_regex_field | account_name |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>'] |
| edit_regex_field | dest_host |  | ['<Data Name(\\)?=(\'|")RemoteMachineAccount(\'|")>({dest_host}[\w\-.]+)'] |
| edit_regex_field | dest_ip |  | ['<Data Name(\\)?=(\'|")RemoteIPAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['<Data Name(\\)?=(\'|")RemoteIPAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '<Data Name(\\)?=(\'|")RemotePort(\'|")>({dest_port}\d+)'] |
| edit_regex_field | dest_user_sid |  | ['<Data Name(\\)?=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^:\s<]+)|({account_domain}[^\\\s<]+)\\+({account_name}[^\s]+)|(?:[^\s\<]+))</Data>'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)</Data>'] |
| edit_regex_field | group_domain |  | ['<Data Name(\\)?=(\'|")TargetDomainName(\'|")>(?=\w)({group_domain}[^<]+)</Data>'] |
| edit_regex_field | group_id |  | ['<Data Name(\\)?=(\'|")TargetSid(\'|")>({group_id}[^<]+)</Data>'] |
| edit_regex_field | group_name |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(?=\w)({group_name}[^<]+)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name(\\)?=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)</Data>'] |
| edit_regex_field | member |  | ['<Data Name(\\)?=(\'|")MemberName(\'|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>', '<Data Name=(\'|")MemberName((\'|")>|":")CN\\?=({member}[^>]+)<\/Data>'] |
| edit_regex_field | process_guid |  | ['<System>.*?Guid(\\)?=(\'|")\{({process_guid}[^}]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}\d+)'] |
| edit_regex_field | src_ip |  | ['<Data Name(\\)?=(\'|")LocalIPAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<'] |
| edit_regex_field | src_port |  | ['<Data Name(\\)?=(\'|")LocalIPAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<', '<Data Name(\\)?=(\'|")LocalPort(\'|")>({src_port}\d+)'] |
| edit_regex_field | thread_id |  | ['ThreadID(\\)?=(\'|")({thread_id}\d+)'] |
| edit_regex_field | time |  | ['SystemTime(\\)?=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_dn |  | ['<Data Name(\\)?=(\'|")MemberName(\'|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>'] |
| edit_regex_field | user_ou |  | ['<Data Name(\\)?=(\'|")MemberName(\'|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name(\\)?=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)</Data>', '<Security UserID(\\)?=(\'|")({user_sid}[^\']+)'] |