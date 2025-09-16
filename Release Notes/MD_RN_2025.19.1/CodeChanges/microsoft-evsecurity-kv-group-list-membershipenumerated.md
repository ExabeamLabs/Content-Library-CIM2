# Code Changes for microsoft-evsecurity-kv-group-list-membershipenumerated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['Process Name:\s+(-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s*(?:\d+|"|,|$)', 'exa_json_path=$.message,exa_regex=Process Name:\s+(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s*("|,|$)'] |
| edit_regex_field | process_name |  | ['Process Name:\s+(-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s*(?:\d+|"|,|$)', 'exa_json_path=$.message,exa_regex=Process Name:\s+(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s*("|,|$)'] |
| edit_regex_field | process_path |  | ['Process Name:\s+(-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s*(?:\d+|"|,|$)', 'exa_json_path=$.message,exa_regex=Process Name:\s+(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/]+?)))\s*("|,|$)'] |