# Code Changes for microsoft-evsecurity-kv-endpoint-success-4624-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name:\s+([A-Fa-f:\d.]+|({src_host_windows}({src_host}[\w\-\.]+)))\s+Source Network'] |
| added_regex_field | src_host |  | ['Workstation Name:\s+([A-Fa-f:\d.]+|({src_host_windows}({src_host}[\w\-\.]+)))\s+Source Network'] |
| removed_attribute | DupFields |  | N/A |