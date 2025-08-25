# Code Changes for unix-unix-mix-user-switch-success-sudo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['\WCOMMAND\\?=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)', '\WPWD\\?=({process_dir}[^\s;]+)'] |
| edit_regex_field | process_name |  | ['\WCOMMAND\\?=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
| edit_regex_field | process_path |  | ['\WCOMMAND\\?=({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |