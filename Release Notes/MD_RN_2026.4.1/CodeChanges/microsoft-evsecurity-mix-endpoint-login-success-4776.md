# Code Changes for microsoft-evsecurity-mix-endpoint-login-success-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'host', 'login_type_text', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |