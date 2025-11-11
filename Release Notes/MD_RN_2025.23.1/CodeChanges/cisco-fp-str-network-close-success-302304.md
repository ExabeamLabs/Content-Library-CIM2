# Code Changes for cisco-fp-str-network-close-success-302304 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'dest_interface', 'dest_ip', 'dest_port', 'duration', 'event_code', 'event_name', 'host', 'operation', 'priority', 'protocol', 'result_reason', 'src_interface', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | action |  | ['({event_name}({action}Teardown)\s+({protocol}[^\s]+).+?connection)', '({operation}({action}Teardown)\s+({protocol}[^\s]+).+?connection)'] |
| edit_regex_field | protocol |  | ['({event_name}({action}Teardown)\s+({protocol}[^\s]+).+?connection)', '({operation}({action}Teardown)\s+({protocol}[^\s]+).+?connection)'] |
| added_regex_field | operation |  | ['({operation}({action}Teardown)\s+({protocol}[^\s]+).+?connection)'] |
| removed_attribute | DupFields |  | N/A |