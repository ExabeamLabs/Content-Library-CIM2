# Code Changes for microsoft-evsecurity-kv-endpoint-success-accountlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(?i)<\d+>\s*\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|\d{4}|({dest_host}({host}[\w.\-]+)))\s'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name=\s*(-|[A-Fa-f:\d.]+|({src_host_windows}({src_host}[^\s;]+)))[\s;]*Source Network Address'] |
| added_regex_field | dest_host |  | ['(?i)<\d+>\s*\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|\d{4}|({dest_host}({host}[\w.\-]+)))\s'] |
| added_regex_field | src_host |  | ['Workstation Name=\s*(-|[A-Fa-f:\d.]+|({src_host_windows}({src_host}[^\s;]+)))[\s;]*Source Network Address'] |
| removed_attribute | DupFields |  | N/A |