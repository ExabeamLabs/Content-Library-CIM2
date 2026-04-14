# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4624-7 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_host', 'dest_ip', 'dest_login_id', 'dest_port', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_name', 'process_path', 'src_host_windows', 'src_ip', 'src_port', 'subject_sid', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |