# Code Changes for microsoft-defenderep-json-alert-trigger-success-devicealertevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'category', 'dest_host', 'dest_ip', 'dest_port', 'operation', 'process_dir', 'process_integrity', 'process_name', 'process_path', 'protocol', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user', 'user_sid'] |
| edit_regex_field | process_dir |  | ['"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"'] |
| edit_regex_field | process_name |  | ['"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"', 'FileName":\s*"({process_name}[^"]+)', 'InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)'] |
| edit_regex_field | process_path |  | ['"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"'] |
| added_regex_field | technique |  | ['"MitreTechniques":"\[({technique}[^\]]+)\]'] |