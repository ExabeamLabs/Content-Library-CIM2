# Code Changes for crowdstrike-falcon-cef-alert-trigger-success-host (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'falcon_host_link', 'file_dir', 'file_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['(?=cs6Label=FalconHostLink).*cs6=({additional_info}({falcon_host_link}.+?))\s+(\w+=|$)', '(\s|\|)cs6=({additional_info}({falcon_host_link}.+?))\s\w+=.*(?=cs6Label=FalconHostLink)', '(\s|\|)msg=({additional_info}.+?)\s+(\w+=|$)'] |
| edit_regex_field | falcon_host_link |  | ['(?=cs6Label=FalconHostLink).*cs6=({additional_info}({falcon_host_link}.+?))\s+(\w+=|$)', '(\s|\|)cs6=({additional_info}({falcon_host_link}.+?))\s\w+=.*(?=cs6Label=FalconHostLink)'] |
| edit_regex_field | file_dir |  | ['(\s|\|)filePath=({process_dir}({file_dir}.+?))\s+(\w+=|$)'] |
| edit_regex_field | file_name |  | ['(\s|\|)fname=({process_name}({file_name}.+?))\s+(\w+=|$)'] |
| added_regex_field | process_dir |  | ['(\s|\|)filePath=({process_dir}({file_dir}.+?))\s+(\w+=|$)'] |
| added_regex_field | process_name |  | ['(\s|\|)fname=({process_name}({file_name}.+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |