# Code Changes for unix-unix-kv-ssh-traffic-audispd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'auth_process', 'dest_host', 'email_address', 'event_code', 'event_name', 'host', 'host_ip', 'login_type_text', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | audispd_type |  | [] |
| added_regex_field | event_name |  | ['\stype=({event_name}USER_\S+)\s+\w+='] |