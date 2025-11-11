# Code Changes for microsoft-evsecurity-kv-endpoint-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_host |  | [',(Audit Success|Success Audit|Information),({dest_host}({host}[\w\-.]+)),'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name:\s+({src_host_windows}({src_host}[\w\-\.]+))\s+Source Network'] |
| added_regex_field | host |  | [',(Audit Success|Success Audit|Information),({dest_host}({host}[\w\-.]+)),'] |
| added_regex_field | src_host |  | ['Workstation Name:\s+({src_host_windows}({src_host}[\w\-\.]+))\s+Source Network'] |
| removed_attribute | DupFields |  | N/A |