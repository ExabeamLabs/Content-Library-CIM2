# Code Changes for microsoft-sysmon-xml-dll-load-7 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'log_name', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'service_state', 'signature', 'signed', 'src_process_name', 'task_name', 'thread_id', 'time', 'user_sid'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>', '<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({src_process_name}({process_name}[^\\\/<>]+?)))<\/Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>', '<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({src_process_name}({process_name}[^\\\/<>]+?)))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>', '<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({src_process_name}({process_name}[^\\\/<>]+?)))<\/Data>'] |
| added_regex_field | src_process_name |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({src_process_name}({process_name}[^\\\/<>]+?)))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |