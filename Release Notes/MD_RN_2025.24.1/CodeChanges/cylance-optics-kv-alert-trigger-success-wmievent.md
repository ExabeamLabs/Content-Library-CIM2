# Code Changes for cylance-optics-kv-alert-trigger-success-wmievent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_domain', 'dest_ip', 'dest_path', 'dest_port', 'device_id', 'domain', 'event_category', 'event_code', 'event_name', 'file_path', 'login_type', 'object', 'operation', 'process_command_line', 'process_name', 'process_owner', 'registry_key', 'registry_path', 'registry_value', 'src_host', 'time', 'user', 'zone'] |
| edit_regex_field | event_category |  | ['Event Type:\s*({alert_type}({event_category}[^,]+))'] |
| added_regex_field | alert_type |  | ['Event Type:\s*({alert_type}({event_category}[^,]+))'] |
| removed_attribute | DupFields |  | N/A |