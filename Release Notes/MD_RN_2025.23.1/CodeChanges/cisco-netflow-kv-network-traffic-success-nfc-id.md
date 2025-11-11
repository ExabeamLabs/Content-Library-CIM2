# Code Changes for cisco-netflow-kv-network-traffic-success-nfc-id (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_port', 'host', 'packets', 'packets_in', 'packets_out', 'protocol', 'src_host', 'src_ip', 'src_port', 'tcp_flags'] |
| added_regex_field | bytes |  | ['\sbytes_in=({bytes}\d+)'] |
| added_regex_field | packets |  | ['\spackets_in=({packets}\d+)'] |
| removed_attribute | DupFields |  | N/A |