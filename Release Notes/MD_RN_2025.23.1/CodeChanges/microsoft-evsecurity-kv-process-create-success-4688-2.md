# Code Changes for microsoft-evsecurity-kv-process-create-success-4688-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'parent_process_guid', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_name', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer(Name)? = "+({src_host}({host}[\w\-.]+))"'] |
| edit_regex_field | process_guid |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| added_regex_field | process_id |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| added_regex_field | src_host |  | ['Computer(Name)? = "+({src_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |