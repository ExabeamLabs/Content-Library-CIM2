# Code Changes for cisco-fp-str-network-traffic-success-teardown-connection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_host', 'dest_translated_ip', 'dest_translated_port', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'icmp_seq_num', 'icmp_type', 'operation', 'priority', 'protocol', 'src_host', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}Teardown ({protocol}\w+) connection))'] |
| edit_regex_field | protocol |  | ['({operation}({event_name}Teardown ({protocol}\w+) connection))'] |
| added_regex_field | operation |  | ['({operation}({event_name}Teardown ({protocol}\w+) connection))'] |
| removed_attribute | DupFields |  | N/A |