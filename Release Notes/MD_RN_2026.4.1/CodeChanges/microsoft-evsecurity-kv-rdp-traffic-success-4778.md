# Code Changes for microsoft-evsecurity-kv-rdp-traffic-success-4778 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |