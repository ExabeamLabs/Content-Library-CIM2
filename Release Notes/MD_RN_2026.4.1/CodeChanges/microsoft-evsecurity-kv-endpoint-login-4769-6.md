# Code Changes for microsoft-evsecurity-kv-endpoint-login-4769-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'service_name', 'src_host', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |