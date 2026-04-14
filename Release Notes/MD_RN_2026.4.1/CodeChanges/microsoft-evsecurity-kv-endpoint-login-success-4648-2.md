# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4648-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'additional_info', 'channel', 'domain', 'event_code', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'session_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['Channel:({channel}[^,]+)'] |