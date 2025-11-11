# Code Changes for microsoft-defenderep-sk4-http-request-browserlaunched (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'host', 'operation', 'parent_process_dir', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'process_path', 'protocol', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| added_regex_field | event_name |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |