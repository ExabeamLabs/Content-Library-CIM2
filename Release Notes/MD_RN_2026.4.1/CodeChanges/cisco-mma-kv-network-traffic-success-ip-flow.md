# Code Changes for cisco-mma-kv-network-traffic-success-ip-flow (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'event_name', 'host', 'protocol', 'src_ip', 'src_mac', 'src_port', 'src_translated_ip', 'src_translated_port', 'time'] |
| edit_regex_field | event_name |  | ['(<\d+>[^\s]+)?\s+({time}\d{10})\.\d+\s({event_name}[^\s]+?)\ssrc=', '({host}[\w.\-]+)\s+({event_name}ip_flow_start)\s+src='] |
| added_regex_field | host |  | ['({host}[\w.\-]+)\s+({event_name}ip_flow_start)\s+src='] |