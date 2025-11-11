# Code Changes for leef-pan-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'device_name', 'domain', 'host', 'network_app', 'process_name', 'protocol', 'result', 'serial_num', 'src_interface', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'threat_category', 'time', 'user'] |
| added_regex_field | device_name |  | ['({device_name}[\w\.-]+)(\s+|,"+)LEEF:', '\|DeviceName=({device_name}[^\|"]+?)\s*(\||"*$)'] |
| removed_attribute | DupFields |  | N/A |