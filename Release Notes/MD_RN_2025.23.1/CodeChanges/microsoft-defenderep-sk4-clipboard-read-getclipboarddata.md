# Code Changes for microsoft-defenderep-sk4-clipboard-read-getclipboarddata (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'operation', 'parent_process_id', 'parent_process_name', 'process_command_line', 'process_id', 'process_integrity', 'process_name', 'protocol', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| added_regex_field | event_name |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |