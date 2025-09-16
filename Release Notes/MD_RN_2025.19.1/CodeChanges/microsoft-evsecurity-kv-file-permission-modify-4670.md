# Code Changes for microsoft-evsecurity-kv-file-permission-modify-4670 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['Process Name:\s*(-|({process_path}({process_dir}.+?[\\\/])?({process_name}[^\\\/\s"]+)))(?:\s+[\w\s]+:|$|")'] |
| edit_regex_field | process_name |  | ['Process Name:\s*(-|({process_path}({process_dir}.+?[\\\/])?({process_name}[^\\\/\s"]+)))(?:\s+[\w\s]+:|$|")'] |
| edit_regex_field | process_path |  | ['Process Name:\s*(-|({process_path}({process_dir}.+?[\\\/])?({process_name}[^\\\/\s"]+)))(?:\s+[\w\s]+:|$|")'] |