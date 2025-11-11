# Code Changes for microsoft-sysmon-mix-registry-create-success-valueset (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'hash_md5', 'host', 'log_name', 'login_id', 'object', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'registry_details', 'registry_details_type', 'registry_key', 'registry_path', 'registry_value', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-\.]+))\sMicrosoft-Windows-Sysmon', 'ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))', '\sComputer="({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-\.]+))\sMicrosoft-Windows-Sysmon', 'ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))', '\sComputer="({dest_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |