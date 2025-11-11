# Code Changes for microsoft-windows-kv-file-write-success-216 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'process_id', 'process_name', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_file_path', 'time'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))\s+({process_name}[^\s]+)\s+'] |
| edit_regex_field | process_name |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))\s+({process_name}[^\s]+)\s+'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))\s+({process_name}[^\s]+)\s+'] |
| removed_attribute | DupFields |  | N/A |