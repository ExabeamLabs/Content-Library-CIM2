# Code Changes for unix-unix-kv-process-create-success-exe (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat | epoch_sec | ['epoch_sec', 'MM/dd/yyyy HH:mm:ss.SSS'] |
| changed | Conditions | [' exe=', ' uid=', 'syscall=', 'type=SYSCALL'] | [' exe=', ' uid=', 'SYSCALL', 'syscall='] |
| changed_parsed_fields | N/A | ['account_id', 'additional_info', 'command_id', 'dest_host', 'group_id', 'host', 'object', 'operation_type', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user_id'] | ['account_id', 'additional_info', 'command_id', 'dest_host', 'failure_code', 'failure_reason', 'group_id', 'host', 'object', 'operation_type', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user_id'] |
| edit_regex_field | time | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w\-.]+)', 'msg=audit\(({time}\d{10})'] | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w\-.]+)', 'msg=audit\(({time}(\d{10})|\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\.\d+)'] |
| added_regex_field | failure_code | [] | ['exit=(\d|({failure_code}[^\(=]+?)\(({failure_reason}[^=]+?))\)\s+\w+='] |
| added_regex_field | failure_reason | [] | ['exit=(\d|({failure_code}[^\(=]+?)\(({failure_reason}[^=]+?))\)\s+\w+='] |
| edit_attribute | activity_type | ['process-create:success'] | ['process-create:fail', 'process-create:success'] |
| edit_attribute | legacy_activity_type | ['process-created'] | ['process-created', 'process-created-failed'] |