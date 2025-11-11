# Code Changes for cisco-mma-kv-alert-trigger-airmarshalevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'aid', 'alert_name', 'alert_type', 'bytes_in', 'channel', 'connection_id', 'dest_mac', 'dhcp_ip', 'duration', 'email_address', 'event_name', 'host', 'is_8021x', 'result_reason', 'session_id', 'src_ip', 'src_mac', 'src_port', 'ssid', 'time', 'user', 'vlan_id'] |
| edit_regex_field | alert_name |  | ['({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({alert_type}({event_name}.+?))\s+\w+='] |
| edit_regex_field | event_name |  | ['({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({alert_type}({event_name}.+?))\s+\w+='] |
| edit_regex_field | host |  | ['({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({alert_type}({event_name}.+?))\s+\w+='] |
| edit_regex_field | time |  | ['({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({alert_type}({event_name}.+?))\s+\w+='] |
| added_regex_field | alert_type |  | ['({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({alert_type}({event_name}.+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |