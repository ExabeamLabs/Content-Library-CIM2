# Code Changes for cisco-asa-str-network-traffic-success-built (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['connection_id', 'dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'dest_translated_host', 'dest_translated_ip', 'dest_translated_port', 'direction', 'email_address', 'event_code', 'event_name', 'host', 'priority', 'protocol', 'src_host', 'src_interface', 'src_ip', 'src_port', 'src_translated_host', 'src_translated_ip', 'src_translated_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['({event_name}Built ({direction}inbound|outbound) ({protocol}TCP|UDP) connection)'] |
| edit_regex_field | protocol |  | ['({event_name}Built ({direction}inbound|outbound) ({protocol}TCP|UDP) connection)'] |
| added_regex_field | direction |  | ['({event_name}Built ({direction}inbound|outbound) ({protocol}TCP|UDP) connection)'] |