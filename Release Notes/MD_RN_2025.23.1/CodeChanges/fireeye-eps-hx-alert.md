# Code Changes for fireeye-eps-hx-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_address', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'malware_file_name', 'malware_url', 'process_dir', 'process_name', 'process_path', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_dir |  | ['filePath=({file_path}(({file_dir}[^=]+[^\\\/])[\\\/]+)?({malware_file_name}({file_name}[^=\\\/]+?)))\s+(\w+=|$)'] |
| edit_regex_field | file_ext |  | ['fname=({malware_file_name}({file_name}[^=]+?(\.({file_ext}[^=\.]+?))?))\s\w+='] |
| edit_regex_field | file_name |  | ['filePath=({file_path}(({file_dir}[^=]+[^\\\/])[\\\/]+)?({malware_file_name}({file_name}[^=\\\/]+?)))\s+(\w+=|$)', 'fname=({malware_file_name}({file_name}[^=]+?(\.({file_ext}[^=\.]+?))?))\s\w+='] |
| edit_regex_field | file_path |  | ['filePath=({file_path}(({file_dir}[^=]+[^\\\/])[\\\/]+)?({malware_file_name}({file_name}[^=\\\/]+?)))\s+(\w+=|$)'] |
| added_regex_field | malware_file_name |  | ['filePath=({file_path}(({file_dir}[^=]+[^\\\/])[\\\/]+)?({malware_file_name}({file_name}[^=\\\/]+?)))\s+(\w+=|$)', 'fname=({malware_file_name}({file_name}[^=]+?(\.({file_ext}[^=\.]+?))?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |