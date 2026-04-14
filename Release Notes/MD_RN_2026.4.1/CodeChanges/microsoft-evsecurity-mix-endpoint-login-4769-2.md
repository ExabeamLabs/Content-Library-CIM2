# Code Changes for microsoft-evsecurity-mix-endpoint-login-4769-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |