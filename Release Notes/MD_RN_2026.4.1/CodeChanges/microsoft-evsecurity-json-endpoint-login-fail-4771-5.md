# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4771-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |