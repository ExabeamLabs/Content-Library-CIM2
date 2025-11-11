# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-auditing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[^\s\/]+))\/Microsoft-Windows-Security-Auditing \(4674\)'] |
| edit_regex_field | process_dir |  | ['Process Name(:|=)\s*(?: |({process_path}({process_dir}(?:[^\";]+))?[\\\/])?({process_name}[^\\\/\";]+?))[\s;]*Requested', '\"ProcessName\":\"(?: |({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))\s*\"'] |
| edit_regex_field | process_name |  | ['Process Name(:|=)\s*(?: |({process_path}({process_dir}(?:[^\";]+))?[\\\/])?({process_name}[^\\\/\";]+?))[\s;]*Requested', '\"ProcessName\":\"(?: |({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))\s*\"'] |
| edit_regex_field | process_path |  | ['Process Name(:|=)\s*(?: |({process_path}({process_dir}(?:[^\";]+))?[\\\/])?({process_name}[^\\\/\";]+?))[\s;]*Requested', '\"ProcessName\":\"(?: |({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))\s*\"'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[^\s\/]+))\/Microsoft-Windows-Security-Auditing \(4674\)'] |
| removed_attribute | DupFields |  | N/A |