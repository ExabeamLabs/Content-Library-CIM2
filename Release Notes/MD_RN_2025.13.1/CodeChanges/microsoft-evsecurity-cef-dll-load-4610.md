# Code Changes for microsoft-evsecurity-cef-dll-load-4610 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_package |  | ['cs5=({file_path}({file_dir}[^<=]+?[\\\/]+)({file_name}[^\\\/<=:]+?))\s*:\s*({auth_package}[^=]+)\s\w+='] |
| edit_regex_field | file_dir |  | ['cs5=({file_path}({file_dir}[^<=]+?[\\\/]+)({file_name}[^\\\/<=:]+?))\s*:\s*({auth_package}[^=]+)\s\w+='] |
| edit_regex_field | file_name |  | ['cs5=({file_path}({file_dir}[^<=]+?[\\\/]+)({file_name}[^\\\/<=:]+?))\s*:\s*({auth_package}[^=]+)\s\w+='] |
| edit_regex_field | file_path |  | ['cs5=({file_path}({file_dir}[^<=]+?[\\\/]+)({file_name}[^\\\/<=:]+?))\s*:\s*({auth_package}[^=]+)\s\w+='] |