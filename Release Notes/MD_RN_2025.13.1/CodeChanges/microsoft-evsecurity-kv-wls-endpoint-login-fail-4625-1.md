# Code Changes for microsoft-evsecurity-kv-wls-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['Opcode.+ProcessName="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+)?({process_name}[^"]+)))"'] |
| edit_regex_field | process_name |  | ['Opcode.+ProcessName="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+)?({process_name}[^"]+)))"'] |
| edit_regex_field | process_path |  | ['Opcode.+ProcessName="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+)?({process_name}[^"]+)))"'] |