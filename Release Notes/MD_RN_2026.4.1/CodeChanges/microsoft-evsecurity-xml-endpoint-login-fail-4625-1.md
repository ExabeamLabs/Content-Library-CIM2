# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'login_type', 'result_code', 'run_level', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |