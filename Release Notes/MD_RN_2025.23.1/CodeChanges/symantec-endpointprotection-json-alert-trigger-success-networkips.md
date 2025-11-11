# Code Changes for symantec-endpointprotection-json-alert-trigger-success-networkips (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'domain', 'host', 'operation', 'os', 'process_dir', 'process_name', 'process_path', 'protocol', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_uid'] |
| added_regex_field | src_host |  | ['"device_name":"({src_host}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |