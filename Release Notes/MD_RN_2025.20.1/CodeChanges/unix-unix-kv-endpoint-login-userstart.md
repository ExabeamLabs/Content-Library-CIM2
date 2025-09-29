# Code Changes for unix-unix-kv-endpoint-login-userstart (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'event_code', 'event_name', 'host', 'host_ip', 'login_type_text', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | audispd_type |  | [] |
| edit_regex_field | event_name |  | ['({event_name}USER_START)', '({event_name}USER_\S+)\s+\w+='] |