# Code Changes for microsoft-evsecurity-xml-endpoint-notification-5031 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |