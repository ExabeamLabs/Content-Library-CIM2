# Code Changes for microsoft-evsecurity-xml-app-notification-success-5056 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | privileges |  | ['<Data Name\\*=(\'|")PrivilegeList(\'|")>({privileges}[^<]+?)<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<'] |