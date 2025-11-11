# Code Changes for microsoft-nps-xml-endpoint-authentication-packettype4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_ip', 'domain', 'email_address', 'event_code', 'host', 'result', 'run_level', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | result |  | ['<Packet-Type[^>]+>({event_code}({result}\d+))'] |
| added_regex_field | event_code |  | ['<Packet-Type[^>]+>({event_code}({result}\d+))'] |
| removed_attribute | DupFields |  | N/A |