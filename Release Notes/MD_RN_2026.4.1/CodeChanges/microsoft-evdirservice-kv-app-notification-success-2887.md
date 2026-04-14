# Code Changes for microsoft-evdirservice-kv-app-notification-success-2887 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'host', 'operation_type', 'result', 'time'] |
| added_regex_field | channel |  | ['Channel=({channel}[^"]+)'] |