# Code Changes for pan-wildfire-cef-alert-trigger-success-wildfirevirusthreat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'device_name', 'domain', 'host', 'malware_url', 'network_app', 'process_name', 'protocol', 'serial_num', 'src_interface', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'time', 'user'] |
| added_regex_field | category |  | ['\|Palo Alto Networks\|PAN-OS\|.*?\|({category}.+?)\|THREAT\|'] |
| added_regex_field | device_name |  | ['dvchost=({device_name}[\w\-\.]+)'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Palo Alto Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address'])]), ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |