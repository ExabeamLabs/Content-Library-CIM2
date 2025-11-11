# Code Changes for microsoft-azure-sk4-network-traffic-nsgflow (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'bytes', 'bytes_in', 'bytes_out', 'category', 'dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'direction', 'event_category', 'event_name', 'host', 'packets', 'packets_in', 'packets_out', 'protocol', 'result', 'src_interface', 'src_ip', 'src_port', 'time'] |
| added_regex_field | bytes |  | ['\scs6=([^,]*,){12}({bytes}\d+)'] |
| added_regex_field | packets |  | ['\scs6=([^,]*,){11}({packets}\d+)'] |
| removed_attribute | DupFields |  | N/A |