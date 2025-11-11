# Code Changes for microsoft-evsecurity-kv-endpoint-success-successfullylogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-\.]+))\/Microsoft-Windows-Security-Auditing \(4624\)', 'Computer:({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-\.]+))\/Microsoft-Windows-Security-Auditing \(4624\)', 'Computer:({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_host |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| removed_attribute | DupFields |  | N/A |