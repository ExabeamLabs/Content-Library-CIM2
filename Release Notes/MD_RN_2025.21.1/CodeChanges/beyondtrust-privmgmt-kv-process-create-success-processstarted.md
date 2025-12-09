# Code Changes for beyondtrust-privmgmt-kv-process-create-success-processstarted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'hash_md5', 'host', 'operation_type', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'token', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| edit_regex_field | process_guid |  | ['Message Description:\s*(<.+?>)?\s+(Unique Process ID:)?\s*({process_id}({process_guid}[^\s]+))\s+Workstyle ID:'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| added_regex_field | process_id |  | ['Message Description:\s*(<.+?>)?\s+(Unique Process ID:)?\s*({process_id}({process_guid}[^\s]+))\s+Workstyle ID:'] |
| removed_attribute | DupFields |  | N/A |