# Code Changes for infoblox-bddi-str-network-notification-removedreversemap (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'host', 'operation', 'process_id', 'process_name', 'src_ip', 'src_port'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Removed reverse map))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Removed reverse map))'] |
| removed_attribute | DupFields |  | N/A |