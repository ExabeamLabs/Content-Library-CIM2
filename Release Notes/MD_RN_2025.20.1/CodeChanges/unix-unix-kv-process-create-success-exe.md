# Code Changes for unix-unix-kv-process-create-success-exe (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'command_id', 'dest_host', 'failure_code', 'failure_reason', 'group_id', 'host', 'object', 'operation_type', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'syscall_name', 'syscall_number', 'system_architecture', 'time', 'user', 'user_id'] |
| edit_regex_field | process_command_line |  | ['\sexe=\\?"({process_command_line}[^"\\]+)\\?"', 'comm="({process_command_line}[^"\\]+)'] |
| added_regex_field | syscall_name |  | ['SYSCALL=({syscall_name}[^"\s]+)'] |
| added_regex_field | syscall_number |  | ['syscall=({syscall_number}\d+)'] |
| added_regex_field | system_architecture |  | ['arch=({system_architecture}[^"\s]+)'] |
| added_regex_field | user |  | ['\sUID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| edit_attribute | activity_type |  | ['process-create:success', 'syscall-execute:fail', 'syscall-execute:success'] |