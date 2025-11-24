# Code Changes for infoblox-bddi-kv-network-notification-reservedrange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'name', 'operation', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Created ReservedRange))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Created ReservedRange))'] |
| removed_attribute | DupFields |  | N/A |