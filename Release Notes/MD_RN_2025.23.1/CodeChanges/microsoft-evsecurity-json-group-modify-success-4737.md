# Code Changes for microsoft-evsecurity-json-group-modify-success-4737 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'process_id', 'result', 'sid_history', 'src_domain', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"', 'exa_regex=Subject:.+?Account Name:\s+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+({src_domain}({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | login_id |  | ['"SubjectLogonId":"({login_id}[^"]+)"', 'exa_regex=Subject:.+?Account Name:\s+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+({src_domain}({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_regex=Subject:.+?Account Name:\s+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+({src_domain}({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"', 'exa_regex=Subject:.+?Account Name:\s+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+({src_domain}({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_regex=Subject:.+?Account Name:\s+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+({src_domain}({domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |