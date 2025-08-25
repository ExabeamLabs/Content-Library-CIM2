# Code Changes for cef-defender-atp-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"'] |
| edit_regex_field | process_name |  | ['"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"', 'InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)'] |
| edit_regex_field | process_path |  | ['"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"'] |