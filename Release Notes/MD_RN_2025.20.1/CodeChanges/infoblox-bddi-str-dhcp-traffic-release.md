# Code Changes for infoblox-bddi-str-dhcp-traffic-release (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'process_id', 'process_name', 'src_ip', 'src_mac', 'src_port', 'time'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |