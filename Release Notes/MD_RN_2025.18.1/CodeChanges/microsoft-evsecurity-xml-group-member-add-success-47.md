# Code Changes for microsoft-evsecurity-xml-group-member-add-success-47 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}[^<]+)<\/Data>'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(\#011)*({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\#\d+)*\s*<'] |
| edit_regex_field | time |  | ['SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<'] |