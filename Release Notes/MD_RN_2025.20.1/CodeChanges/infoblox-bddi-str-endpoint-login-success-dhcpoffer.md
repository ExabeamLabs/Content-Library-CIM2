# Code Changes for infoblox-bddi-str-endpoint-login-success-dhcpoffer (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_interface', 'dest_ip', 'dest_mac', 'dest_port', 'event_name', 'host', 'ip_lease_time', 'process_id', 'process_name', 'src_ip', 'time', 'user_id'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |