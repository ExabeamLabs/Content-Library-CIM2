# Code Changes for unix-unix-kv-endpoint-login-success-userauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'email_address', 'event_name', 'host', 'host_ip', 'process_dir', 'process_id', 'result', 'session_id', 'src_host', 'src_ip', 'time', 'user', 'user_id'] |
| removed_regex_field | audispd_type |  | [] |
| added_regex_field | event_name |  | ['\stype=({event_name}USER_\S+)\s+\w+='] |