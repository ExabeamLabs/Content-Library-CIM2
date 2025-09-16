# Code Changes for microsoft-evsecurity-xml-user-lock-success-4740 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(?=\w)({domain}[^<]+)</Data>', '<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)</Data>'] |
| edit_regex_field | host |  | ['<Computer>({host}[\w\-.]+)</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] |
| removed_regex_field | src_domain |  | [] |
| removed_regex_field | src_user |  | [] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| added_regex_field | account |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({account}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| added_regex_field | src_host |  | ['<Data Name=(\'|")TargetDomainName(\'|")>(?:\\+)?({src_host}[\w\-\.]+)</Data>'] |
| removed_attribute | DupFields |  | N/A |