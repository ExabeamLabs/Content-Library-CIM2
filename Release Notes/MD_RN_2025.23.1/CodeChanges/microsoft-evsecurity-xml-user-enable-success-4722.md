# Code Changes for microsoft-evsecurity-xml-user-enable-success-4722 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))<', 'Subject:.+?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:'] |
| edit_regex_field | host |  | ['<Computer>({host}({src_host}[\w\-\.]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))<'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<', 'Subject:.+?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:'] |
| added_regex_field | src_host |  | ['<Computer>({host}({src_host}[\w\-\.]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |