# Code Changes for microsoft-defenderep-json-app-login-success-timegenerated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'event_name', 'hash_md5', 'host', 'parent_process_name', 'process_command_line', 'process_id', 'process_integrity', 'process_name', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | category |  | ['"Type"+:\s*"+({event_name}({category}[^",]+))'] |
| added_regex_field | event_name |  | ['"Type"+:\s*"+({event_name}({category}[^",]+))'] |
| removed_attribute | DupFields |  | N/A |