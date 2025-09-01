# Code Changes for microsoft-defenderep-cef-process-create-success-processcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | parent_process_name |  | ['"InitiatingProcessParentFileName":\s*"({parent_process_name}[^"]+)'] |
| edit_regex_field | process_dir |  | ['"FolderPath"+:\s*"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"', '"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))'] |
| edit_regex_field | process_name |  | ['"FileName\\?"+:\s*\\?"+(|({process_name}[^"]+?))\\?,*"', '"FolderPath"+:\s*"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"', '"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))', 'InitiatingProcessFileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?","'] |
| edit_regex_field | process_path |  | ['"FolderPath"+:\s*"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"', '"InitiatingProcessFolderPath":\s*"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))'] |