# Code Changes for fortinet-firewall-kv-network-traffic-notice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'bytes_in', 'bytes_out', 'dest_country', 'dest_host', 'dest_interface', 'dest_interface_role', 'dest_ip', 'dest_mac', 'dest_port', 'domain', 'email_address', 'event_category', 'host', 'operation', 'packets_sent', 'policy_id', 'policy_name', 'protocol', 'src_country', 'src_host', 'src_host_type', 'src_interface', 'src_interface_role', 'src_ip', 'src_mac', 'src_port', 'src_translated_ip', 'time', 'tz', 'url', 'user'] |
| edit_regex_field | src_mac |  | ['\Wsrcmac="?({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"?', '\ssrcmac="?({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"?'] |
| added_regex_field | dest_mac |  | ['\Wdstmac="?({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"?'] |
| added_regex_field | src_host_type |  | ['\Wsrchwvendor=\"+({src_host_type}[^"]+)'] |
| added_regex_field | src_translated_ip |  | ['\Wtransip=(::ffff:)?({src_translated_ip}[a-fA-F\d.:]+)'] |