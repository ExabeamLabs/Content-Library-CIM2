# Code Changes for microsoft-evsecurity-json-endpoint-login-4769-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'service_name', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid', 'user_upn', 'web_domain'] |
| added_regex_field | channel |  | ['channel\\?"+:\\?"+({channel}[^"\\]+)'] |