# Code Changes for microsoft-defenderep-json-alert-trigger-success-devicealertevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'operation', 'process_dir', 'process_integrity', 'process_name', 'process_path', 'protocol', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user', 'user_sid'] |
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| added_regex_field | alert_type |  | ['category"+:\s*"+({alert_type}[^"]+)'] |
| added_regex_field | event_name |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |