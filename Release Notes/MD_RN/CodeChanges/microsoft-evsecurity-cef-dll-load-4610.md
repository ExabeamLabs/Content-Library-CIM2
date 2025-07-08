# Code Changes for microsoft-evsecurity-cef-dll-load-4610 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['aid', 'auth_package', 'd_name', 'd_parent', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'process_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'thread_id', 'time', 'user'] | ['aid', 'auth_package', 'd_name', 'd_parent', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'full_name', 'host', 'login_id', 'process_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'thread_id', 'time', 'user'] |
| edit_regex_field | auth_package | ['cs5=({auth_package}[^=]+?)\s\w+='] | ['cs5=({file_path}({file_dir}[^<=]+?)[\\\/]+)({file_name}[^\\\/<=:]+?)\s*:\s*({auth_package}[^=]+)\s\w+='] |
| added_regex_field | file_dir | [] | ['cs5=({file_path}({file_dir}[^<=]+?)[\\\/]+)({file_name}[^\\\/<=:]+?)\s*:\s*({auth_package}[^=]+)\s\w+='] |
| added_regex_field | file_name | [] | ['cs5=({file_path}({file_dir}[^<=]+?)[\\\/]+)({file_name}[^\\\/<=:]+?)\s*:\s*({auth_package}[^=]+)\s\w+='] |
| added_regex_field | file_path | [] | ['cs5=({file_path}({file_dir}[^<=]+?)[\\\/]+)({file_name}[^\\\/<=:]+?)\s*:\s*({auth_package}[^=]+)\s\w+='] |