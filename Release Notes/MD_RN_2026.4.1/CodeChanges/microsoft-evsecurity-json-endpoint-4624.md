# Code Changes for microsoft-evsecurity-json-endpoint-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['channel\\?"+:\\?"+({channel}[^"\\]+)\\?"'] |