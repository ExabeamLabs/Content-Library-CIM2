# Code Changes for unix-unix-kv-process-create-success-command (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'current_working_dir', 'error_code', 'host', 'host_ip', 'process_command_line', 'process_name', 'process_relative_dir', 'process_relative_path', 'src_host', 'time', 'user'] |
| removed_regex_field | process_dir |  | [] |
| edit_regex_field | process_name |  | ['\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
| removed_regex_field | process_path |  | [] |
| added_regex_field | current_working_dir |  | ['\WPWD\\?=({current_working_dir}[^\s;=]+?)[\s;]*\w+='] |
| added_regex_field | process_relative_dir |  | ['\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
| added_regex_field | process_relative_path |  | ['\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |