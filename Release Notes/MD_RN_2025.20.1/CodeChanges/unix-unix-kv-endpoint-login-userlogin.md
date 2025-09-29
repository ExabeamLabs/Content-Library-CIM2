# Code Changes for unix-unix-kv-endpoint-login-userlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'auth_process', 'event_code', 'event_name', 'host', 'host_ip', 'login_type_text', 'process_id', 'result', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_id'] |
| removed_regex_field | audispd_type |  | [] |
| edit_regex_field | event_name |  | ['({event_name}USER_LOGIN)', '\stype=({event_name}USER_\S+)\s+\w+='] |