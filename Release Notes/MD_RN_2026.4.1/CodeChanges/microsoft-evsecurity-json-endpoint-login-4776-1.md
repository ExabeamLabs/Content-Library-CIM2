# Code Changes for microsoft-evsecurity-json-endpoint-login-4776-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"'] |