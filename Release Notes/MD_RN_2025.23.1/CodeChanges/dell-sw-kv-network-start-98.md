# Code Changes for dell-sw-kv-network-start-98 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category_id', 'dest_interface', 'dest_ip', 'dest_mac', 'dest_port', 'email_address', 'event_code', 'event_name', 'firewall', 'message_id', 'packets_in', 'packets_out', 'priority', 'protocol', 'rule', 'severity', 'src_interface', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | message_id |  | ['\sm=({alert_type}({message_id}\d+))'] |
| added_regex_field | alert_type |  | ['\sm=({alert_type}({message_id}\d+))'] |
| added_regex_field | event_code |  | ['\sm=({event_code}\d+)'] |
| added_regex_field | priority |  | ['\spri=({priority}\d+)'] |
| removed_attribute | DupFields |  | N/A |