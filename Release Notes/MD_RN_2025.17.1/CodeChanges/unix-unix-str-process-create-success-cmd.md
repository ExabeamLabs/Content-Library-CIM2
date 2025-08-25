# Code Changes for unix-unix-str-process-create-success-cmd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'host', 'host_ip', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | process_command_line |  | ['CMD = ({process_command_line}[^;]+?)\s*(;|$|")', '\sCMD \(\s*({process_command_line}.+?)\)($|\s|")', '\sCMD\s+\=?\s*({process_command_line}.+?)$'] |
| edit_regex_field | process_dir |  | ['PWD = ({process_dir}[^\s,=;]+)', '\WCMD\s+({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s=]+))\s(?:|;|$)'] |
| added_regex_field | process_name |  | ['\WCMD\s+({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s=]+))\s(?:|;|$)'] |
| added_regex_field | process_path |  | ['\WCMD\s+({process_path}({process_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s=]+))\s(?:|;|$)'] |