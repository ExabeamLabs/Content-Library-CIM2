# Code Changes for microsoft-defenderep-sk4-process-create-success-processcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | parent_process_dir |  | ['"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+[\\\/]+)?({parent_process_name}[^"\\\/]+))"'] |
| edit_regex_field | parent_process_name |  | ['"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+[\\\/]+)?({parent_process_name}[^"\\\/]+))"'] |
| edit_regex_field | parent_process_path |  | ['"InitiatingProcessParentFileName":"({parent_process_path}({parent_process_dir}[^"]+[\\\/]+)?({parent_process_name}[^"\\\/]+))"'] |
| edit_regex_field | process_dir |  | ['"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"', '"InitiatingProcessFolderPath"+:\s*"+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"'] |
| edit_regex_field | process_name |  | ['"FileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?,"', '"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"', '"InitiatingProcessFolderPath"+:\s*"+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"', 'InitiatingProcessFileName\\?"+:\s*\\?"+({process_name}[^"\\\/]+?)\\?"'] |
| edit_regex_field | process_path |  | ['"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"', '"InitiatingProcessFolderPath"+:\s*"+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"'] |