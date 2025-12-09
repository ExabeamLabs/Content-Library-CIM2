# Code Changes for tanium-ep-json-alert-trigger-success-accountenumeration (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'path', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'user'] |
| edit_regex_field | process_dir |  | ['exa_json_path=$.[\'Match Details\'].match..file.fullpath,exa_regex=({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))'] |
| edit_regex_field | process_name |  | ['exa_json_path=$.[\'Match Details\'].match..file.fullpath,exa_regex=({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))'] |
| edit_regex_field | process_path |  | ['exa_json_path=$.[\'Match Details\'].match..file.fullpath,exa_regex=({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))'] |
| added_regex_field | path |  | ['exa_json_path=$.[\'Match Details\'].match..file.fullpath,exa_regex=({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))'] |
| removed_attribute | DupFields |  | N/A |