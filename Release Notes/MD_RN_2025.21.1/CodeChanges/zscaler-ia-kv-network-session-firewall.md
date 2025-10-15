# Code Changes for zscaler-ia-kv-network-session-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'bytes_in', 'bytes_out', 'category', 'department', 'dest_country', 'dest_ip', 'dest_port', 'dest_service_name', 'duration', 'email_address', 'host', 'location', 'network_app', 'owner_id', 'protocol', 'result', 'rule', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'threat_category', 'time', 'user', 'vpn_client_type'] |
| edit_regex_field | result |  | ['action=({action}({result}[^\s]+))'] |
| added_regex_field | action |  | ['action=({action}({result}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |