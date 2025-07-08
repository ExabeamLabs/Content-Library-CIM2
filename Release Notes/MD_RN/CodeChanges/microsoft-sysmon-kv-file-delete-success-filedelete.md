# Code Changes for microsoft-sysmon-kv-file-delete-success-filedelete (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir | ['Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s]+))\s+\w+:'] | ['Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s\\\/]+))\s+\w+:'] |
| edit_regex_field | process_name | ['Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s]+))\s+\w+:'] | ['Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s\\\/]+))\s+\w+:'] |
| edit_regex_field | process_path | ['Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s]+))\s+\w+:'] | ['Image:\s+({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^\s\\\/]+))\s+\w+:'] |