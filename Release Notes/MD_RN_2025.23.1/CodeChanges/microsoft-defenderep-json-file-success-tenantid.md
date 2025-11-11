# Code Changes for microsoft-defenderep-json-file-success-tenantid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'category', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'hash_md5', 'host', 'parent_process_name', 'process_command_line', 'process_id', 'process_integrity', 'process_name', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | result |  | ['ActionType_s"+:\s*"+({access}({result}[^",]+))'] |
| added_regex_field | access |  | ['ActionType_s"+:\s*"+({access}({result}[^",]+))'] |
| removed_attribute | DupFields |  | N/A |