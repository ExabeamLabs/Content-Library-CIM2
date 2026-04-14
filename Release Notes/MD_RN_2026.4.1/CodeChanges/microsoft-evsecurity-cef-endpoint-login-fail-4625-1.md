# Code Changes for microsoft-evsecurity-cef-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'failure_reason', 'host', 'login_id', 'login_type', 'result', 'result_code', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"'] |