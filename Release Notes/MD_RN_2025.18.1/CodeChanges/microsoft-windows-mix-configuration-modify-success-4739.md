# Code Changes for microsoft-windows-mix-configuration-modify-success-4739 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<EventID>4739<', 'Domain Policy was changed', 'SubjectUserName'] |
| edit_regex_field | domain |  | ['<Data Name\\?=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\?=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<\/Data>'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}[^"\']+)'] |
| edit_regex_field | thread_id |  | ['ThreadID\\?=(\'|")({thread_id}\d+)'] |
| edit_regex_field | user |  | ['<Data Name\\?=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\?=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<\/Data>'] |