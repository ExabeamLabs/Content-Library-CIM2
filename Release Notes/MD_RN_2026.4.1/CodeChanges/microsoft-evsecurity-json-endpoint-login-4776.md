# Code Changes for microsoft-evsecurity-json-endpoint-login-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'login_type_text', 'result', 'result_code', 'src_host', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |