# Code Changes for microsoft-evsecurity-json-endpoint-login-4768-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |