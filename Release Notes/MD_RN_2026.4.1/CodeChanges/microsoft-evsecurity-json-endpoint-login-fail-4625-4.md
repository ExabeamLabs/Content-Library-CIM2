# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4625-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'key_length', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['Channel\\?"+:\\?"+({channel}[^"\\]+)'] |