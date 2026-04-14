# Code Changes for microsoft-evsystem-kv-endpoint-logout-success-40 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'src_port', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['channel="({channel}[^"]+)'] |