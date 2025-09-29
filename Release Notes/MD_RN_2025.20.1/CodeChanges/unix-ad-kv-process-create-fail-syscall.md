# Code Changes for unix-ad-kv-process-create-fail-syscall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'failure_reason', 'group_id', 'host', 'operation_type', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'session_id', 'syscall_name', 'syscall_number', 'system_architecture', 'time', 'user', 'user_id'] |
| added_regex_field | process_command_line |  | ['comm="({process_command_line}[^"\\]+)'] |
| added_regex_field | syscall_name |  | ['SYSCALL=({syscall_name}[^"\s]+)'] |
| added_regex_field | syscall_number |  | ['syscall=({syscall_number}\d+)'] |
| added_regex_field | system_architecture |  | ['arch=({system_architecture}[^"\s]+)'] |
| added_regex_field | user |  | ['\sUID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| edit_attribute | activity_type |  | ['syscall-execute:fail'] |