# Code Changes for sap-s-cef-file-download-success-download (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_dir |  | ['fname=({file_path}({file_dir}[^"]+?[\\\/]+)(\\|({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)?))\s*$'] |
| edit_regex_field | file_ext |  | ['fname=({file_path}({file_dir}[^"]+?[\\\/]+)(\\|({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)?))\s*$'] |
| edit_regex_field | file_name |  | ['fname=({file_path}({file_dir}[^"]+?[\\\/]+)(\\|({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)?))\s*$'] |
| edit_regex_field | file_path |  | ['fname=({file_path}({file_dir}[^"]+?[\\\/]+)(\\|({file_name}[^"\\\/]+?(\.({file_ext}\w+))?)?))\s*$'] |