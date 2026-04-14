# Code Changes for microsoft-evsecurity-json-endpoint-logout-success-4779-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'channel', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'provider_name', 'session_name', 'severity', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |