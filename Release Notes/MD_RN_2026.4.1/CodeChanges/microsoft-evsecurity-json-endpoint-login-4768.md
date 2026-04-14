# Code Changes for microsoft-evsecurity-json-endpoint-login-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_type', 'channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |