# Code Changes for microsoft-azure-kv-file-success-vmid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'domain', 'event_category', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'login_id', 'operation', 'parent_process_name', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_category |  | ['category\":\"({category}({event_category}[^\"]+))'] |
| added_regex_field | category |  | ['category\":\"({category}({event_category}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |