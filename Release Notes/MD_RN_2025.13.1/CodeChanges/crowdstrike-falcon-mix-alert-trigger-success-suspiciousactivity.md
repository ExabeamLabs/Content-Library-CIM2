# Code Changes for crowdstrike-falcon-mix-alert-trigger-success-suspiciousactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['"CommandLine":"+({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+\.exe))[^"]*?"', '"CommandLine":"\\"({process_path}({process_dir}[^"]+?)\\{1,2}({process_name}[^\\"]+))\\"'] |
| edit_regex_field | process_name |  | ['"CommandLine":"+({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+\.exe))[^"]*?"', '"CommandLine":"\\"({process_path}({process_dir}[^"]+?)\\{1,2}({process_name}[^\\"]+))\\"', '"FileName":\s*"({process_name}[^"]+)"'] |
| edit_regex_field | process_path |  | ['"CommandLine":"+({process_path}({process_dir}[^"]+?[\\\/]+)({process_name}[^"\\\/]+\.exe))[^"]*?"', '"CommandLine":"\\"({process_path}({process_dir}[^"]+?)\\{1,2}({process_name}[^\\"]+))\\"'] |