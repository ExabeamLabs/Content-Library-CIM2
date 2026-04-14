# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4625-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_package', 'auth_process', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'key_length', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |