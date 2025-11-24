# Code Changes for infoblox-bddi-str-network-notification-success-deltadiskopen (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'host', 'operation', 'process_id', 'process_name', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Non-empty delta disk being open))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Non-empty delta disk being open))'] |
| removed_attribute | DupFields |  | N/A |