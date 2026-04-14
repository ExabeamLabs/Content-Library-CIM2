# Code Changes for microsoft-evsecurity-json-network-session-fail-4653 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'channel', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'failure_reason', 'host', 'src_ip', 'src_port', 'time'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |