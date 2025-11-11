# Code Changes for vmware-carbonblackappctrl-json-process-close-success-deviceexternalip (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'dest_ip', 'dest_port', 'device_id', 'domain', 'event_category', 'host', 'operation_type', 'os', 'parent_process_command_line', 'parent_process_guid', 'parent_process_id', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | event_category |  | ['"+type"+:"+({operation_type}({event_category}[^"]+))"+'] |
| added_regex_field | operation_type |  | ['"+type"+:"+({operation_type}({event_category}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |