# Code Changes for microsoft-evsecurity-kv-process-create-success-processcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'parent_process_guid', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_name', 'user'] |
| edit_regex_field | process_guid |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| added_regex_field | process_id |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| removed_attribute | DupFields |  | N/A |