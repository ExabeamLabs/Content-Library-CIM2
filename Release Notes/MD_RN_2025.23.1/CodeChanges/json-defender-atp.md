# Code Changes for json-defender-atp (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'dest_host', 'dest_ip', 'dest_port', 'device_class', 'device_description', 'device_id', 'domain', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'full_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'operation', 'os', 'parent_process_dir', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'service_name', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | action |  | ['ActionType":\s*"({operation}({action}[^"]+))'] |
| edit_regex_field | category |  | ['category":\s*"({event_name}({category}[^"]+))'] |
| edit_regex_field | operation |  | ['ActionType":\s*"({operation}({action}[^"]+))', 'operationName":\s*"({operation}[^"]+)'] |
| added_regex_field | event_name |  | ['category":\s*"({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |