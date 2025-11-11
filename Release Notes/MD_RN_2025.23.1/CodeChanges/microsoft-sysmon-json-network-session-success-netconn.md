# Code Changes for microsoft-sysmon-json-network-session-success-netconn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'path', 'process_dir', 'process_id', 'process_name', 'process_path', 'user'] |
| edit_regex_field | process_dir |  | ['exa_regex=\"Image\":\"({path}({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+)))\"'] |
| edit_regex_field | process_name |  | ['exa_regex=\"Image\":\"({path}({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+)))\"'] |
| edit_regex_field | process_path |  | ['exa_regex=\"Image\":\"({path}({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+)))\"'] |
| added_regex_field | path |  | ['exa_regex=\"Image\":\"({path}({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+)))\"'] |
| removed_attribute | DupFields |  | N/A |