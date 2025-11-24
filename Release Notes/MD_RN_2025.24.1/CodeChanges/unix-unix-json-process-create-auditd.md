# Code Changes for unix-unix-json-process-create-auditd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_id', 'arg', 'dest_host', 'group_id', 'host', 'operation_type', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user', 'user_id'] |
| edit_regex_field | host |  | ['"host":\{.*?"name":"(|({dest_host}({host}[^"]+)))"'] |
| added_regex_field | dest_host |  | ['"host":\{.*?"name":"(|({dest_host}({host}[^"]+)))"'] |
| removed_attribute | DupFields |  | N/A |