# Code Changes for crowdstrike-falcon-json-process-create-success-deliverlocalfxtocloud (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'aid', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha256', 'old_hash', 'os', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['"event_simpleName":\s*"({event_code}({event_name}[^"]+))', '"name":\s*"({event_code}({event_name}[^"]+))'] |
| added_regex_field | event_code |  | ['"event_simpleName":\s*"({event_code}({event_name}[^"]+))', '"name":\s*"({event_code}({event_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |