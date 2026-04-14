# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'result_code', 'run_level', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |