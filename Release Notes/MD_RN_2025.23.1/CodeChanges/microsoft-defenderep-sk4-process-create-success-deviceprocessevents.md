# Code Changes for microsoft-defenderep-sk4-process-create-success-deviceprocessevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'operation', 'parent_process_name', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| added_regex_field | event_name |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |