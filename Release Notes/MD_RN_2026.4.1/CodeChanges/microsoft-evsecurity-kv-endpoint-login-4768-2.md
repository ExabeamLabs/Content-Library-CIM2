# Code Changes for microsoft-evsecurity-kv-endpoint-login-4768-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |