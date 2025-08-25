# Code Changes for microsoft-evsecurity-xml-configuration-modify-success-4716 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)</Data>'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)'] |