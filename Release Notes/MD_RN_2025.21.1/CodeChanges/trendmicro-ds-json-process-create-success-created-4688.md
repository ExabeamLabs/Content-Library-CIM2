# Code Changes for trendmicro-ds-json-process-create-success-created-4688 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_category', 'event_code', 'event_name', 'host', 'login_id', 'os', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_guid', 'process_id', 'src_host', 'src_ip', 'tenant_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | parent_process_guid |  | ['Creator Process ID:\s*({parent_process_id}({parent_process_guid}[^\\\s;]+))(\s|;|\\)'] |
| edit_regex_field | process_guid |  | ['New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_id}({process_guid}[^\\\s;]+))(\s|;|\\)'] |
| added_regex_field | parent_process_id |  | ['Creator Process ID:\s*({parent_process_id}({parent_process_guid}[^\\\s;]+))(\s|;|\\)'] |
| added_regex_field | process_id |  | ['New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_id}({process_guid}[^\\\s;]+))(\s|;|\\)'] |
| removed_attribute | DupFields |  | N/A |