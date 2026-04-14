# Code Changes for microsoft-evsecurity-json-rdp-traffic-success-4778 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | channel |  | ['"channel\\?":\\?"({channel}[^"\\]+)'] |