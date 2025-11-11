# Code Changes for cisco-asa-str-network-traffic-success-teardown (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_host', 'dest_translated_ip', 'dest_translated_port', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'icmp_seq_num', 'icmp_type', 'operation', 'priority', 'protocol', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | protocol |  | ['({event_name}Teardown ({protocol}\w+) connection)', '({operation}Teardown ({protocol}\w+) connection)'] |
| added_regex_field | operation |  | ['({operation}Teardown ({protocol}\w+) connection)'] |
| removed_attribute | DupFields |  | N/A |