# Code Changes for microsoft-evsecurity-xml-share-delete-success-5144 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<\/Data>'] |
| edit_regex_field | share_name |  | ['<Data Name\\*=(\'|")ShareName(\'|")>(?:[\\\*]+)?({share_name}[^<]+)<\/Data>'] |
| edit_regex_field | share_path |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>({share_path}[^<]+)<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |