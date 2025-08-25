# Code Changes for pan-ngfw-csv-network-traffic-success-end (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'bytes_in', 'bytes_out', 'category', 'dest_country', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'dest_user', 'device_name', 'email_address', 'event_category', 'host', 'network_app', 'protocol', 'result_reason', 'rule', 'serial_num', 'session_id', 'src_country', 'src_domain', 'src_interface', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'src_user', 'subtype', 'time', 'virtual_station_name'] |
| added_regex_field | virtual_station_name |  | [',TRAFFIC,([^,]*,){11}({virtual_station_name}[^,\s]+?)\s*,'] |