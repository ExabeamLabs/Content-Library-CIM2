# Code Changes for unix-unix-kv-endpoint-notification-proctitle (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_category', 'event_name', 'host', 'host_ip', 'operation_type', 'time'] |
| edit_regex_field | event_category |  | ['type=({operation_type}({event_category}[^=]+?))\s+(\w+=|$)'] |
| added_regex_field | operation_type |  | ['type=({operation_type}({event_category}[^=]+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |