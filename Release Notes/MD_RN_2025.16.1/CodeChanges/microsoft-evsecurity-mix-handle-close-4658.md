# Code Changes for microsoft-evsecurity-mix-handle-close-4658 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({domain}[^<>]+))</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)</Data>'] |
| edit_regex_field | object_id |  | ['<Data Name\\*=(\'|")HandleId(\'|")>({object_id}[^<>]+)</Data>'] |
| edit_regex_field | object_server |  | ['<Data Name\\*=(\'|")ObjectServer(\'|")>({object_server}[^<>]+)</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}[^<>]+)</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<>]+)</Data>'] |