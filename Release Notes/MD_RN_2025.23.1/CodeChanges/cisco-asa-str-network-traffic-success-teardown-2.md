# Code Changes for cisco-asa-str-network-traffic-success-teardown-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'connection_id', 'dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'domain', 'duration', 'email_address', 'email_domain', 'event_code', 'event_name', 'host', 'operation', 'priority', 'protocol', 'result_reason', 'src_host', 'src_interface', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | protocol |  | ['({event_name}Teardown ({protocol}\w+) connection)', '({operation}Teardown ({protocol}\w+) connection)'] |
| added_regex_field | operation |  | ['({operation}Teardown ({protocol}\w+) connection)'] |
| removed_attribute | DupFields |  | N/A |