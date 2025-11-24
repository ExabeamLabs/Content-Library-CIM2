# Code Changes for infoblox-bddi-str-network-notification-removedforwardmap (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'event_name', 'host', 'operation', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port'] |
| edit_regex_field | operation |  | ['({event_name}({operation}Removed forward map))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}Removed forward map))'] |
| removed_attribute | DupFields |  | N/A |