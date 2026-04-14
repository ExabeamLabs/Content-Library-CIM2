# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4648-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'account_login_guid', 'auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_host', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_login_guid', 'user_sid'] |
| added_regex_field | channel |  | ['"channel\\?":\\?"({channel}[^"\\]+)'] |