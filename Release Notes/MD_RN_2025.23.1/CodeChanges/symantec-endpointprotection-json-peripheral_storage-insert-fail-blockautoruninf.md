# Code Changes for symantec-endpointprotection-json-peripheral_storage-insert-fail-blockautoruninf (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'app', 'bytes', 'domain', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'operation', 'os', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_uid'] |
| added_regex_field | src_host |  | ['"device_name":"({src_host}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |