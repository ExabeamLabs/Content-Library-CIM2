# Code Changes for microsoft-sysmon-json-registry-12 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'severity', 'target', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | file_dir |  | ['"TargetObject":"({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?)))\s*"'] |
| edit_regex_field | file_name |  | ['"TargetObject":"({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?)))\s*"'] |
| edit_regex_field | file_path |  | ['"TargetObject":"({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?)))\s*"'] |
| edit_regex_field | host |  | ['"Hostname":"({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | dest_host |  | ['"Hostname":"({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | target |  | ['"TargetObject":"({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?)))\s*"'] |
| removed_attribute | DupFields |  | N/A |