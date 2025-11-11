# Code Changes for microsoft-sysmon-kv-registry-modify-success-registryvalueset (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'file_dir', 'file_name', 'file_path', 'host', 'operation', 'operation_type', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['\sComputer(?:Name)?=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\sComputer(?:Name)?=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |