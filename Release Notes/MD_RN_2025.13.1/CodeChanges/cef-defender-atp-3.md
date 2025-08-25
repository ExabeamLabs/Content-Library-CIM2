# Code Changes for cef-defender-atp-3 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | parent_process_dir |  | ['"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+?[\\\/]+)?({parent_process_name}[^"\\\/]+))"'] |
| edit_regex_field | parent_process_name |  | ['"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+?[\\\/]+)?({parent_process_name}[^"\\\/]+))"'] |
| edit_regex_field | parent_process_path |  | ['"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+?[\\\/]+)?({parent_process_name}[^"\\\/]+))"'] |
| edit_regex_field | process_dir |  | ['"InitiatingProcessFolderPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))"'] |
| edit_regex_field | process_name |  | ['"InitiatingProcessFolderPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))"', 'InitiatingProcessFileName"+:\s*"+({process_name}[\w\.\-]+)"'] |
| edit_regex_field | process_path |  | ['"InitiatingProcessFolderPath":\s*"(({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+(\.[a-zA-Z]+)))|({=process_dir}[^"]+))"'] |