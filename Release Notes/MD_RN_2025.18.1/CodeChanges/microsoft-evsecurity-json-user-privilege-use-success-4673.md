# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-4673 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+?)</Data>', '<Data Name\\*=(\'|")SubjectUserSid(\'|")>\s*(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+?)</Data>'] |
| edit_regex_field | object_server |  | ['<Data Name\\*=(\'|")ObjectServer(\'|")>({object_server}[^<]+?)</Data>'] |
| edit_regex_field | privileges |  | ['<Data Name\\*=(\'|")PrivilegeList(\'|")>({privileges}[^<]+?)</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>', '<Data Name\\*=(\'|")SubjectUserSid(\'|")>\s*(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |