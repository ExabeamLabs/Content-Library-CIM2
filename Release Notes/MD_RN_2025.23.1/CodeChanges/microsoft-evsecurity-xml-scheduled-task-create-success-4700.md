# Code Changes for microsoft-evsecurity-xml-scheduled-task-create-success-4700 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_user', 'task_name', 'time', 'user'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))<'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[^<]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[^<]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))<'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |