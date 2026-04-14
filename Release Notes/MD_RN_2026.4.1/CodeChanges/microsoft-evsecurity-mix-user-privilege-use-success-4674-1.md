# Code Changes for microsoft-evsecurity-mix-user-privilege-use-success-4674-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'object', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |