# Code Changes for microsoft-evsecurity-xml-endpoint-login-success-4624-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'dest_login_id', 'domain', 'event_code', 'event_id', 'event_name', 'full_name', 'host', 'key_length', 'login_id', 'login_type', 'object', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'run_level', 'src_host_windows', 'src_ip', 'src_port', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | dest_login_id |  | ['Linked Logon ID(:|=)\s*(\\[nrt])*({dest_login_id}[^\s\\;]+)\s*'] |