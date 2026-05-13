# Code Changes for unix-unixdhcpd-str-dhcp-session-success-dhcpd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | [' dhcpd', ': Forward map from '] |
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_ip', 'dest_port', 'host', 'process_id', 'process_name', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |