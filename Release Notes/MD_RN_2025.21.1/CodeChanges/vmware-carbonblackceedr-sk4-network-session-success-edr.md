# Code Changes for vmware-carbonblackceedr-sk4-network-session-success-edr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'email_address', 'event_name', 'host', 'operation_type', 'os', 'parent_cmd', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'status_msg', 'time', 'user'] |
| edit_regex_field | event_name |  | ['"+type"+:\s*"+({operation_type}({event_name}[^"]+?))"+'] |
| added_regex_field | operation_type |  | ['"+type"+:\s*"+({operation_type}({event_name}[^"]+?))"+'] |
| removed_attribute | DupFields |  | N/A |