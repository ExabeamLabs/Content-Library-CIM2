# Code Changes for zlock-z-cef-app-activity-success-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['app', 'bytes', 'device_name', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'policy_name', 'process_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] | ['app', 'bytes', 'device_name', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'policy_name', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | process_name | ['sproc=({process_name}[^\s]+)\s+(\w+=|$)'] | ['sproc=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)'] |
| added_regex_field | process_dir | [] | ['sproc=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)'] |
| added_regex_field | process_path | [] | ['sproc=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)'] |