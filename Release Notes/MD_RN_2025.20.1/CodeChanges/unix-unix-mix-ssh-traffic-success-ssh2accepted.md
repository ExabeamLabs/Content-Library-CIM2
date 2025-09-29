# Code Changes for unix-unix-mix-ssh-traffic-success-ssh2accepted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'auth', 'dest_host', 'dest_ip', 'domain', 'event_code', 'host', 'host_ip', 'login_id', 'process_id', 'process_name', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |