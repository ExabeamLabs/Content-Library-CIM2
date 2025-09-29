# Code Changes for unix-dhcpd-str-dhcp-discover-nofreeleases (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_interface', 'dest_ip', 'dest_mac', 'event_name', 'host', 'process_id', 'process_name', 'service_id'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |