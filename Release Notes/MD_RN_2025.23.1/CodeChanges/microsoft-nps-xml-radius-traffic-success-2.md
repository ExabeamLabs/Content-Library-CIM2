# Code Changes for microsoft-nps-xml-radius-traffic-success-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'auth_type', 'dest_host', 'dest_ip', 'domain', 'event_code', 'host', 'network', 'result', 'run_level', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | result |  | ['<Packet-Type.+?>({event_code}({result}\d+))'] |
| added_regex_field | event_code |  | ['<Packet-Type.+?>({event_code}({result}\d+))'] |
| removed_attribute | DupFields |  | N/A |