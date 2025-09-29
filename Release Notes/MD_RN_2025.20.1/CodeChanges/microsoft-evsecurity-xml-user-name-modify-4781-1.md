# Code Changes for microsoft-evsecurity-xml-user-name-modify-4781-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(-|({dest_domain}[^<]+))<'] |
| edit_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(-|({dest_user_sid}[^<]+))<'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(-|({domain}[^<]+))<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>(-|({login_id}[^<]+))<'] |
| edit_regex_field | new_user_name |  | ['<Data Name\\*=(\'|")NewTargetUserName(\'|")>(-|({new_user_name}[^<]+))<'] |
| edit_regex_field | old_user_name |  | ['<Data Name\\*=(\'|")OldTargetUserName(\'|")>(-|({old_user_name}[^<]+))<'] |
| edit_regex_field | privileges |  | ['<Data Name\\*=(\'|")PrivilegeList(\'|")>(-|({privileges}[^<]+))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>(-|({user_sid}[^<]+))<'] |