# Code Changes for microsoft-evsecurity-xml-dll-load-4610 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['auth_package', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'src_host', 'thread_id', 'time'] | ['auth_package', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'process_id', 'result', 'run_level', 'src_host', 'thread_id', 'time'] |
| edit_regex_field | auth_package | ['<Data Name\\*=(\'|")AuthenticationPackageName(\'|")>({auth_package}[^<]+)<'] | ['<Data Name\\*=(\'|")AuthenticationPackageName(\'|")>({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)'] |
| added_regex_field | file_dir | [] | ['<Data Name\\*=(\'|")AuthenticationPackageName(\'|")>({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)'] |
| added_regex_field | file_name | [] | ['<Data Name\\*=(\'|")AuthenticationPackageName(\'|")>({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)'] |
| added_regex_field | file_path | [] | ['<Data Name\\*=(\'|")AuthenticationPackageName(\'|")>({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)'] |