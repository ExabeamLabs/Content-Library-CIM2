# Code Changes for cisco-asa-str-network-traffic-success-built (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['connection_id', 'dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'dest_translated_host', 'dest_translated_ip', 'dest_translated_port', 'email_address', 'event_code', 'event_name', 'host', 'priority', 'protocol', 'src_host', 'src_interface', 'src_ip', 'src_port', 'src_translated_host', 'src_translated_ip', 'src_translated_port', 'time', 'user'] |
| removed_regex_field | direction |  | [] |
| edit_regex_field | event_name |  | ['({event_name}Built (inbound|outbound) ({protocol}TCP|UDP) connection)'] |
| edit_regex_field | protocol |  | ['({event_name}Built (inbound|outbound) ({protocol}TCP|UDP) connection)'] |