# Code Changes for sentinelone-singularityp-json-process-create-success-process (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'dest_domain', 'dest_host', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'dest_process_publisher', 'dest_user', 'dest_user_full_name', 'device_type', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'grandparent_process_path', 'hash_sha1', 'hash_sha256', 'host', 'host_type', 'os', 'parent_process_command_line', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'parent_process_publisher', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'process_publisher', 'process_signed', 'time', 'user'] |
| edit_regex_field | host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | Platform |  | ['MacOS', 'SentinelOne', 'Unix', 'Windows'] |