# Code Changes for microsoft-evsecurity-xml-share-modify-success-5143 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<Data Name', '<EventID>5143', 'SubjectUserSid'] |
| edit_regex_field | d_name |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))<'] |
| edit_regex_field | d_parent |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))<'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<'] |
| edit_regex_field | file_type |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({file_type}[^<]+)<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | share_name |  | ['<Data Name\\*=(\'|")ShareName(\'|")>(?:[\\\*]+)?({share_name}[^<]+)<'] |
| edit_regex_field | share_path |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<'] |