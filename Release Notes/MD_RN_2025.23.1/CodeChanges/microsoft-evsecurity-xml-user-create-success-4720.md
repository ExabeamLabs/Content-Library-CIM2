# Code Changes for microsoft-evsecurity-xml-user-create-success-4720 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | account_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({account_domain}[^<]+))</Data>'] |
| edit_regex_field | account_name |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({account_name}[^<]+))</Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(?=\w)({src_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[\w\-.]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(?=\w)((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({account_domain}[^<]+))</Data>'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({account_name}[^<]+))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(?=\w)({src_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | src_host |  | ['<Computer>({src_host}({host}[\w\-.]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(?=\w)((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |