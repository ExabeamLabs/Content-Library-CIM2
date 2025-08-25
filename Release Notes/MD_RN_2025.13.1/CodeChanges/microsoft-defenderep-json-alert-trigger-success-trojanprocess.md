# Code Changes for microsoft-defenderep-json-alert-trigger-success-trojanprocess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['exa_json_path=$.process,exa_regex=({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+))'] |
| edit_regex_field | process_name |  | ['exa_json_path=$.process,exa_regex=({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+))'] |
| edit_regex_field | process_path |  | ['exa_json_path=$.process,exa_regex=({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+))'] |