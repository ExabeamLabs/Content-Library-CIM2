# Code Changes for microsoft-evsecurity-xml-user-privilege-assign-success-4704 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | privileges |  | ['<Data Name\\*=(\'|")PrivilegeList(\'|")>({privileges}[^<]+?)<'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}[^"\']+)'] |
| edit_regex_field | provider_name |  | ['<Provider Name\\*=(\'|")({provider_name}[^\'"]+)(\'|")'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}[^\'"]+)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<'] |