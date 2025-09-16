# Code Changes for microsoft-evsecurity-kv-group-member-list-4799 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['Process Name:\s*(-|({process_path}({process_dir}.*?[\\\/])?({process_name}[^\\\/\s"]+)))(?:\s+[\\w\s]+|:|$|")', 'exa_json_path=$..CallerProcessName,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$'] |
| edit_regex_field | process_id |  | ['Process ID:\s*({process_id}[\w]+)\s+'] |
| edit_regex_field | process_name |  | ['Process Name:\s*(-|({process_path}({process_dir}.*?[\\\/])?({process_name}[^\\\/\s"]+)))(?:\s+[\\w\s]+|:|$|")', 'exa_json_path=$..CallerProcessName,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$'] |
| edit_regex_field | process_path |  | ['Process Name:\s*(-|({process_path}({process_dir}.*?[\\\/])?({process_name}[^\\\/\s"]+)))(?:\s+[\\w\s]+|:|$|")', 'exa_json_path=$..CallerProcessName,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$'] |