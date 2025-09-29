# Code Changes for unix-unix-kv-ssh-traffic-sshuserauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'auth', 'auth_process', 'dest_host', 'dest_ip', 'email_address', 'event_code', 'event_name', 'host', 'login_type_text', 'process_dir', 'process_id', 'result', 'session_id', 'src_host', 'src_ip', 'time', 'user', 'user_id'] |
| removed_regex_field | audispd_type |  | [] |
| added_regex_field | event_name |  | ['\stype=({event_name}USER_\S+)\s+\w+='] |
| removed_attribute | DupFields |  | N/A |