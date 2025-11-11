# Code Changes for microsoft-evsecurity-xml-user-lock-success-4740 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| removed_regex_field | account |  | [] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")TargetDomainName(\'|")>(?:\\+)?({domain}[\w\-\.]+)</Data>'] |
| removed_regex_field | src_host |  | [] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(?=\w)({src_domain}[^<]+)</Data>', '<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}[^<]+)</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |