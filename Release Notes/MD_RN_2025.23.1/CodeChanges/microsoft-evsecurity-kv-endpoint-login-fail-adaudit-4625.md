# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_code', 'event_id', 'host', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['SOURCE\s*=\s*({src_host_windows}({src_host}[\w\-.]+))'] |
| added_regex_field | src_host |  | ['SOURCE\s*=\s*({src_host_windows}({src_host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |