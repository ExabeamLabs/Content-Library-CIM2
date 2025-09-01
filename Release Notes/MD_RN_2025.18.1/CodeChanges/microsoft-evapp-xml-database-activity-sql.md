# Code Changes for microsoft-evapp-xml-database-activity-sql (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_process_dir |  | ['<Data Name\\*=(\'|")TargetProcessName(\'|")>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | dest_process_name |  | ['<Data Name\\*=(\'|")TargetProcessName(\'|")>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | dest_process_path |  | ['<Data Name\\*=(\'|")TargetProcessName(\'|")>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name(\\)?=(\'|")ProcessId(\'|")>({process_id}[^<]+?)\s*<', "<Execution ProcessID(\\)?='({process_id}[^']+)"] |
| edit_regex_field | process_name |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>', "<Message>Process '?({process_name}[^\s']+)"] |
| edit_regex_field | process_path |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>'] |
| edit_regex_field | thread_id |  | ['ThreadID(\\)?=(\'|")({thread_id}\d+)'] |