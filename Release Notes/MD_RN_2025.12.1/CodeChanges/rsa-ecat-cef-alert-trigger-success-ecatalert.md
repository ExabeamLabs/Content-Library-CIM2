# Code Changes for rsa-ecat-cef-alert-trigger-success-ecatalert (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'malware_url', 'process_name', 'threat_category'] | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'malware_url', 'process_dir', 'process_name', 'process_path', 'threat_category'] |
| edit_regex_field | process_name | ['\sfname=({process_name}.+?)\s+(\w+=|$)'] | ['\sfname=({process_name}.+?)\s+(\w+=|$)', '\stargetModule=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)'] |
| added_regex_field | process_dir | [] | ['\stargetModule=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)'] |
| added_regex_field | process_path | [] | ['\stargetModule=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)'] |