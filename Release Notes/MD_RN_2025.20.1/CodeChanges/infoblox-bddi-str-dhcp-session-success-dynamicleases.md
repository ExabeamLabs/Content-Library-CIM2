# Code Changes for infoblox-bddi-str-dhcp-session-success-dynamicleases (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_mac', 'dest_port', 'event_name', 'host', 'operation', 'process_id', 'process_name', 'src_ip', 'src_port'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |