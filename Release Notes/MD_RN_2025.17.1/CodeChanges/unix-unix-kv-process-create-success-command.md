# Code Changes for unix-unix-kv-process-create-success-command (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'error_code', 'host', 'host_ip', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'src_host', 'time', 'user'] |
| edit_regex_field | process_dir |  | ['\WCOMMAND\\?=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)', '\WPWD\\?=({process_dir}[^\s;=]+?)[\s;]*\w+='] |
| added_regex_field | process_name |  | ['\WCOMMAND\\?=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
| added_regex_field | process_path |  | ['\WCOMMAND\\?=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |