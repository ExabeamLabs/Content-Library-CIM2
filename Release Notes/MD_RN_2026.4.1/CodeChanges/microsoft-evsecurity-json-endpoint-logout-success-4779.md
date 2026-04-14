# Code Changes for microsoft-evsecurity-json-endpoint-logout-success-4779 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'severity', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel\\?":\\?"({channel}[^"\\]+)'] |