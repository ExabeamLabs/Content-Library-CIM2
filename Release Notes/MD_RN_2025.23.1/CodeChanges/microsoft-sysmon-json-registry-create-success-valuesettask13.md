# Code Changes for microsoft-sysmon-json-registry-create-success-valuesettask13 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'log_name', 'object', 'operation', 'process_guid', 'process_id', 'process_name', 'process_path', 'registry_key', 'registry_path', 'registry_value', 'time', 'user', 'user_sid'] |
| edit_regex_field | file_dir |  | ['\"Image\":\s*\"[\\?]*({process_path}({file_path}({file_dir}[^\"]*?[\\\/]+)?({process_name}({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))))\"'] |
| edit_regex_field | file_ext |  | ['\"Image\":\s*\"[\\?]*({process_path}({file_path}({file_dir}[^\"]*?[\\\/]+)?({process_name}({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))))\"'] |
| edit_regex_field | file_name |  | ['\"Image\":\s*\"[\\?]*({process_path}({file_path}({file_dir}[^\"]*?[\\\/]+)?({process_name}({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))))\"'] |
| edit_regex_field | file_path |  | ['\"Image\":\s*\"[\\?]*({process_path}({file_path}({file_dir}[^\"]*?[\\\/]+)?({process_name}({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))))\"'] |
| edit_regex_field | host |  | ['\"Hostname\":\s*\"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | operation |  | ['\"Message\":\s*\"({event_name}({operation}[^:]+))'] |
| added_regex_field | dest_host |  | ['\"Hostname\":\s*\"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | event_name |  | ['\"Message\":\s*\"({event_name}({operation}[^:]+))'] |
| added_regex_field | process_name |  | ['\"Image\":\s*\"[\\?]*({process_path}({file_path}({file_dir}[^\"]*?[\\\/]+)?({process_name}({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))))\"'] |
| added_regex_field | process_path |  | ['\"Image\":\s*\"[\\?]*({process_path}({file_path}({file_dir}[^\"]*?[\\\/]+)?({process_name}({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))))\"'] |
| removed_attribute | DupFields |  | N/A |