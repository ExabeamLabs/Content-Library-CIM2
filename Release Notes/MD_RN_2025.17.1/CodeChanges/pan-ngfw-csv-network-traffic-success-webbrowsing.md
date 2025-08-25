# Code Changes for pan-ngfw-csv-network-traffic-success-webbrowsing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_ip', 'dest_network_zone', 'dest_port', 'domain', 'event_category', 'host', 'policy_name', 'protocol', 'result_code', 'rule', 'src_host', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'time', 'user', 'virtual_station_name'] |
| edit_regex_field | dest_port |  | [',DECRYPTION,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),(?:[^,]*,){3}(?:|({protocol}[^,]+)),({result_code}[^,]+),'] |
| edit_regex_field | protocol |  | [',DECRYPTION,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),(?:[^,]*,){3}(?:|({protocol}[^,]+)),({result_code}[^,]+),'] |
| removed_regex_field | result |  | [] |
| edit_regex_field | src_port |  | [',DECRYPTION,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),(?:[^,]*,){3}(?:|({protocol}[^,]+)),({result_code}[^,]+),'] |
| added_regex_field | result_code |  | [',DECRYPTION,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),(?:[^,]*,){3}(?:|({protocol}[^,]+)),({result_code}[^,]+),'] |
| added_regex_field | virtual_station_name |  | [',DECRYPTION,([^,]*,){11}({virtual_station_name}[^,]+?)\s*,'] |