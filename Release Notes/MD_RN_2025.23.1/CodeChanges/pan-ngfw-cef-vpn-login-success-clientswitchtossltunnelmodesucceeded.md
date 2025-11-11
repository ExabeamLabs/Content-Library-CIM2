# Code Changes for pan-ngfw-cef-vpn-login-success-clientswitchtossltunnelmodesucceeded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes_in', 'bytes_out', 'category', 'dest_host', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'direction', 'domain', 'event_category', 'host', 'network_app', 'profile', 'protocol', 'result', 'result_reason', 'rule', 'severity', 'src_host', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'subtype', 'time', 'user'] |
| added_regex_field | action |  | ['\|({action}[^\|]+)\|TRAFFIC'] |
| removed_attribute | DupFields |  | N/A |