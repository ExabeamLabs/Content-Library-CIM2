# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4770 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |