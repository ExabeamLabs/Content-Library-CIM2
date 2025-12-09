# Code Changes for fortinet-firewall-kv-network-traffic-notice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'bytes_in', 'bytes_out', 'dest_country', 'dest_host', 'dest_interface', 'dest_interface_role', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_category', 'host', 'operation', 'packets_sent', 'policy_id', 'policy_name', 'protocol', 'src_country', 'src_host', 'src_interface', 'src_interface_role', 'src_ip', 'src_mac', 'src_port', 'time', 'tz', 'url', 'user'] |
| added_regex_field | bytes |  | ['\Wrcvdbyte=({bytes}\d+)'] |
| removed_attribute | DupFields |  | N/A |