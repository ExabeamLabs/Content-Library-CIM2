# Code Changes for microsoft-evsecurity-xml-registry-create-success-4657 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^\<]+)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^\<]+)</Data>'] |
| edit_regex_field | object_id |  | ['<Data Name\\*=(\'|")HandleId(\'|")>({object_id}[^\<]+)</Data>'] |
| edit_regex_field | old_registry_details |  | ['<Data Name\\*=(\'|")OldValue(\'|")>(-|({old_registry_details}[^\<]+))</Data>'] |
| edit_regex_field | old_registry_details_type |  | ['<Data Name\\*=(\'|")OldValueType(\'|")>(-|({old_registry_details_type}[^\<]+))</Data>'] |
| edit_regex_field | operation |  | ['<Data Name\\*=(\'|")OperationType(\'|")>({operation}[^\<]+)</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}[^\<]+)</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")ProcessName(\'|")>({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))</Data>'] |
| edit_regex_field | registry_details |  | ['<Data Name\\*=(\'|")NewValue(\'|")>(-|({registry_details}[^\<]+))</Data>', '<Data Name\\*=(\'|")OperationType(\'|").+?(1906|delete).+?(\'|")OldValueType(\'|")>({registry_details_type}[^<]+?)<.+?(\'|")OldValue(\'|")>({registry_details}[^<]+)'] |
| edit_regex_field | registry_details_type |  | ['<Data Name\\*=(\'|")NewValueType(\'|")>(-|({registry_details_type}[^\<]+))</Data>', '<Data Name\\*=(\'|")OperationType(\'|").+?(1906|delete).+?(\'|")OldValueType(\'|")>({registry_details_type}[^<]+?)<.+?(\'|")OldValue(\'|")>({registry_details}[^<]+)'] |
| edit_regex_field | registry_key |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({registry_path}[^\<]*?({registry_key}[^\<\\\/]+))<\/Data>'] |
| edit_regex_field | registry_path |  | ['<Data Name\\*=(\'|")ObjectName(\'|")>({registry_path}[^\<]*?({registry_key}[^\<\\\/]+))<\/Data>'] |
| edit_regex_field | registry_value |  | ['<Data Name\\*=(\'|")ObjectValueName(\'|")>({registry_value}[^\<]+)<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^\<]+)</Data>'] |
| edit_attribute | activity_type |  | ['registry-create:success', 'registry-delete:success', 'registry-modify:success'] |