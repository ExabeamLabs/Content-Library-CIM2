# Code Changes for microsoft-evsecurity-kv-process-create-success-mswineventlog4688 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_name', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['(?:Success|Audit)\s+\w+\s+({src_host}({host}[\w\-.]+))', 'Information\s+({src_host}({host}[\w.\-]+))\s+'] |
| edit_regex_field | process_guid |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| added_regex_field | process_id |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| added_regex_field | src_host |  | ['(?:Success|Audit)\s+\w+\s+({src_host}({host}[\w\-.]+))', 'Information\s+({src_host}({host}[\w.\-]+))\s+'] |
| removed_attribute | DupFields |  | N/A |