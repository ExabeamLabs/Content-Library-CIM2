# Code Changes for microsoft-windows-kv-process-create-success-processid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'time'] |
| edit_regex_field | host |  | ['Host="({dest_host}({host}[^"]+))'] |
| edit_regex_field | process_guid |  | ['ProcessId=({process_id}({process_guid}.+?))\s+(\w+=|$)'] |
| added_regex_field | dest_host |  | ['Host="({dest_host}({host}[^"]+))'] |
| added_regex_field | process_id |  | ['ProcessId=({process_id}({process_guid}.+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |