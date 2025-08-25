# Code Changes for microsoft-sysmon-xml-alert-trigger-success-25 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['<Data Name=(\'|")Image(\'|")>({process_path}({process_dir}[^<>"]*?[\\\/]+)?({process_name}[^"<>\\\/\']*))<\/Data>'] |
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\'"}]+)'] |
| edit_regex_field | process_id |  | ['ProcessID\\*=(\'|")({process_id}\d+)(\'|")'] |
| edit_regex_field | process_name |  | ['<Data Name=(\'|")Image(\'|")>({process_path}({process_dir}[^<>"]*?[\\\/]+)?({process_name}[^"<>\\\/\']*))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name=(\'|")Image(\'|")>({process_path}({process_dir}[^<>"]*?[\\\/]+)?({process_name}[^"<>\\\/\']*))<\/Data>'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\']+)(\'|")'] |