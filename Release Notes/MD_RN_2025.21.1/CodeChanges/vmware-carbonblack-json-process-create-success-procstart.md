# Code Changes for vmware-carbonblack-json-process-create-success-procstart (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'dest_ip', 'dest_port', 'device_id', 'domain', 'event_name', 'host', 'operation_type', 'os', 'parent_process_command_line', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user'] |
| added_regex_field | event_name |  | ['"type":"({event_name}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |