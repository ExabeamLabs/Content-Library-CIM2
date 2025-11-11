# Code Changes for microsoft-defenderep-kv-alert-trigger-success-syscenterendpointprotection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'file_name', 'process_name', 'process_path', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['dest_name=({src_host}({dest_host}[\w\-.]+))\s'] |
| edit_regex_field | dest_ip |  | ['user_id=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+dest_ip=({src_ip}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s+'] |
| edit_regex_field | process_name |  | ['process="({process_path}[^"]+\\({file_name}({process_name}[^"]+)))"'] |
| edit_regex_field | process_path |  | ['process="({process_path}[^"]+\\({file_name}({process_name}[^"]+)))"'] |
| edit_regex_field | user |  | ['user_id=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+dest_ip=({src_ip}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s+'] |
| added_regex_field | file_name |  | ['process="({process_path}[^"]+\\({file_name}({process_name}[^"]+)))"'] |
| added_regex_field | src_host |  | ['dest_name=({src_host}({dest_host}[\w\-.]+))\s'] |
| added_regex_field | src_ip |  | ['user_id=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+dest_ip=({src_ip}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s+'] |
| removed_attribute | DupFields |  | N/A |