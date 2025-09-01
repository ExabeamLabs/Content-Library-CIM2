# Code Changes for microsoft-evsecurity-xml-group-modify-success-4735-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | group_id |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>({group_id}[^<]+)'] |
| edit_regex_field | group_name |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({group_name}[^<]+)', '<Data Name\\*=(\'|")TargetUserName(\'|")>({group_name}[^<]+)'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<\/Data>'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)'] |
| changed | Conditions |  | ['<Computer>', '<Data Name', '<EventID>4735</EventID>', 'SubjectUserName', 'TargetUserName'] |