# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4770-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |