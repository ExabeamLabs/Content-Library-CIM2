# Code Changes for microsoft-evsecurity-kv-network-listen-5154 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'channel', 'event_code', 'event_name', 'host', 'process_id', 'protocol', 'src_ip', 'src_port', 'time'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |