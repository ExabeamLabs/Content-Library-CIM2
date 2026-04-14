# Code Changes for microsoft-evsecurity-kv-driver-load-fail-5038-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'host', 'operation_type', 'result', 'time'] |
| added_regex_field | channel |  | ['Channel=({channel}[^"]+)'] |