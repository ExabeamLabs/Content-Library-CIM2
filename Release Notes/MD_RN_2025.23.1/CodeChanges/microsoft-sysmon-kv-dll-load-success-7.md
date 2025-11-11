# Code Changes for microsoft-sysmon-kv-dll-load-success-7 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha256', 'host', 'imphash', 'path', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'signed', 'time', 'user'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| removed_attribute | DupFields |  | N/A |