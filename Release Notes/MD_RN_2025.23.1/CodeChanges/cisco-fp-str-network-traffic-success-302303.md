# Code Changes for cisco-fp-str-network-traffic-success-302303 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_interface', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'host', 'operation', 'priority', 'protocol', 'src_interface', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | protocol |  | ['({event_name}Built ({protocol}TCP|UDP).+?connection)', '({operation}Built ({protocol}TCP|UDP).+?connection)'] |
| added_regex_field | operation |  | ['({operation}Built ({protocol}TCP|UDP).+?connection)'] |
| removed_attribute | DupFields |  | N/A |