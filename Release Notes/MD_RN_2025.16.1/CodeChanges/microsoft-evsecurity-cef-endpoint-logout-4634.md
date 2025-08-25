# Code Changes for microsoft-evsecurity-cef-endpoint-logout-4634 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_domain |  | ['<Data Name=(\'|")TargetDomainName(\'|")>({dest_domain}[^<]+)<'] |
| edit_regex_field | dest_login_id |  | ['<Data Name\\=(\'|")TargetLogonId(\'|")>({dest_login_id}[^<]+)<'] |
| edit_regex_field | dest_user |  | ['<Data Name=(\'|")TargetUserName(\'|")>(SYSTEM|({dest_user}[^<]+))<'] |
| edit_regex_field | dest_user_sid |  | ['<Data Name\\=(\'|")TargetUserSid(\'|")>({dest_user_sid}[^<]+)<'] |
| edit_regex_field | login_id |  | ['<Data Name\\=(\'|")SubjectLogonId(\'|")>(-|({login_id}[^<>]+))<'] |
| edit_regex_field | login_type |  | ['<Data Name\\=(\'|")LogonType(\'|")>({login_type}\d+)<'] |
| edit_regex_field | process_dir |  | ['<Data Name\\=(\'|")(Caller)?ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<'] |
| edit_regex_field | process_id |  | ['<Data Name\\=(\'|")(Caller)?ProcessId(\'|")>({process_id}[^<]+?)\s*<', '<Execution ProcessID\\=(\'|")({process_id}[^\'"]+)'] |
| edit_regex_field | process_name |  | ['<Data Name\\=(\'|")(Caller)?ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<'] |
| edit_regex_field | process_path |  | ['<Data Name\\=(\'|")(Caller)?ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<'] |
| edit_regex_field | src_domain |  | ['<Data Name\\=(\'|")SubjectDomainName(\'|")>(-|({src_domain}[^<>]+))<'] |
| edit_regex_field | src_user |  | ['<Data Name\\=(\'|")SubjectUserName(\'|")>(-|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | time |  | ['<TimeCreated SystemTime\\=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})'] |
| edit_regex_field | user_sid |  | ['<Data Name\\=(\'|")SubjectUserSid(\'|")>(-|({user_sid}[^<>]+))<'] |