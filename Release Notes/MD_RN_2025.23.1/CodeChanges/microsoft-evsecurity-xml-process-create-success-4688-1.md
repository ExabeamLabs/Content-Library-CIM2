# Code Changes for microsoft-evsecurity-xml-process-create-success-4688-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'service_name', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<', 'Account Domain:\s*(|-|NT AUTHORITY|({domain}[^:]+?))\s*Logon ID:'] |
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[\w\-.]+))<', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | process_guid |  | ['<Data Name\\*=(\'|")NewProcessId(\'|")>\s*({process_id}({process_guid}[x\da-f]+))<', 'New Process ID:\s*({process_id}({process_guid}[x\da-f]+))'] |
| edit_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<', 'Account Name:\s*(|-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:'] |
| added_regex_field | process_id |  | ['<Data Name\\*=(\'|")NewProcessId(\'|")>\s*({process_id}({process_guid}[x\da-f]+))<', 'New Process ID:\s*({process_id}({process_guid}[x\da-f]+))'] |
| added_regex_field | src_host |  | ['<Computer>({src_host}({host}[\w\-.]+))<', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |