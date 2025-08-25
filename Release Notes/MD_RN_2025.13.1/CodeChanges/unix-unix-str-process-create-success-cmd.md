# Code Changes for unix-unix-str-process-create-success-cmd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | [' CMD ', ']: '] |
| changed_parsed_fields | N/A |  | ['account', 'host', 'host_ip', 'process_command_line', 'process_dir', 'time', 'user'] |
| edit_regex_field | process_command_line |  | ['CMD = ({process_command_line}[^;]+?)\s*(;|$|")', '\sCMD \(\s*({process_command_line}.+?)\)($|\s|")'] |
| added_regex_field | host_ip |  | ['from_remote_host = ({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| added_regex_field | process_dir |  | ['PWD = ({process_dir}[^\s,=;]+)'] |
| added_regex_field | user |  | ['USER = ({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |