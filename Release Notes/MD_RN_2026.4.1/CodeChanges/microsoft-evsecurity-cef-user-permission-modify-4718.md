# Code Changes for microsoft-evsecurity-cef-user-permission-modify-4718 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_type', 'channel', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_full_name', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'file_path', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'return_code', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |