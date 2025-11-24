# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'operation', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}An account was successfully logged on))'] |
| added_regex_field | operation |  | ['({operation}({event_name}An account was successfully logged on))'] |