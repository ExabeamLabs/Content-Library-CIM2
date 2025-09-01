# Code Changes for microsoft-evsecurity-xml-handle-request-success-4659 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | access |  | ['<Data Name\\*=(\'|")DesiredAccess(\'|")>({access}[^<]+?)\s*<\/Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | file_dir |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({file_path}({file_dir}[^<]+)\/({file_name}[^<]+\.({file_ext}[^<]+)))<\/Data>'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({file_path}({file_dir}[^<]+)\/({file_name}[^<]+\.({file_ext}[^<]+)))<\/Data>'] |
| edit_regex_field | file_name |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({file_path}({file_dir}[^<]+)\/({file_name}[^<]+\.({file_ext}[^<]+)))<\/Data>'] |
| edit_regex_field | file_path |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({file_path}({file_dir}[^<]+)\/({file_name}[^<]+\.({file_ext}[^<]+)))<\/Data>'] |
| edit_regex_field | object |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({object}[^<]+)<\/Data>'] |
| edit_regex_field | object_class |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({object_class}[^<]+)<\/Data>'] |
| edit_regex_field | object_id |  | ['<Data Name\\*=(\'|")HandleId(\'|")>({object_id}[^<]+)<\/Data>'] |
| edit_regex_field | object_server |  | ['<Data Name\\*=(\'|")ObjectServer(\'|")>({object_server}[^<]+)<\/Data>'] |
| edit_regex_field | time |  | ['TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<\/Data>'] |