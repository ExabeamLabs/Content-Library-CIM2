# Code Changes for trendmicro-officescan-leef-network-session-fail-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'bytes_in', 'bytes_out', 'dest_ip', 'dest_mac', 'dest_port', 'event_name', 'host', 'protocol', 'src_ip', 'src_mac', 'src_port'] |
| edit_regex_field | alert_name |  | ['\Wname=({event_name}({alert_name}.+?))\s*(\w+=|$)'] |
| added_regex_field | event_name |  | ['\Wname=({event_name}({alert_name}.+?))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |