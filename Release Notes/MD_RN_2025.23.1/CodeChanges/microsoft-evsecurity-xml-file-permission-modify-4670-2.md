# Code Changes for microsoft-evsecurity-xml-file-permission-modify-4670-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'login_id', 'new_attribute', 'object_id', 'object_name', 'object_server', 'object_type', 'old_attribute', 'permissions', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+)))</Data>'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | file_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| added_regex_field | file_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| added_regex_field | file_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>(-|({file_path}({process_path}(({file_dir}({process_dir}[^<>]+?))[\\\/]+)?({file_name}({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+)))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |