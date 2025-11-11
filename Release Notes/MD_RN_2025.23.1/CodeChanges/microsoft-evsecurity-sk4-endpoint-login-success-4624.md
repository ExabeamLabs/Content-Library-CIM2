# Code Changes for microsoft-evsecurity-sk4-endpoint-login-success-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'subject_sid', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(::ffff:)?({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| added_regex_field | src_host |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(::ffff:)?({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*Source Network Address(:|=)'] |
| removed_attribute | DupFields |  | N/A |