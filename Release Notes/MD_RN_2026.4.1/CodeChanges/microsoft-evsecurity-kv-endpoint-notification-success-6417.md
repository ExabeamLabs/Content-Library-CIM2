# Code Changes for microsoft-evsecurity-kv-endpoint-notification-success-6417 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'host', 'operation_type', 'result', 'time'] |
| added_regex_field | channel |  | ['Channel=({channel}[^"]+)'] |