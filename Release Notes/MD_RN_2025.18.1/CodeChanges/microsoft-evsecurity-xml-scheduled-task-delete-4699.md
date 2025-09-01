# Code Changes for microsoft-evsecurity-xml-scheduled-task-delete-4699 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({domain}[^<]+?))<', '<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)', 'Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | login_id |  | ['<Data Name(\\)?=(\'|")SubjectLogonId(\'|")>(-|({login_id}[^<]+?))<', '<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)', 'Logon ID:\s*({login_id}\S+)\s+'] |
| edit_regex_field | task_name |  | ['<Data Name\\*=(\'|")TaskName(\'|")>({task_name}[^<]+)', 'Task Name:\s*(|-|({task_name}[^:]+?))\s*Task Content:'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', '<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)', '<Security UserID(\\)?=(\'|")({user_sid}[^\'"]+)', 'Security ID:\s*({user_sid}\S+)\s+Account Name:'] |