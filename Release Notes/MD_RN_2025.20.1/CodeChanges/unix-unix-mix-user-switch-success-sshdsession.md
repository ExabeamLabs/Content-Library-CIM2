# Code Changes for unix-unix-mix-user-switch-success-sshdsession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_user_id', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'process_name', 'project_id', 'time', 'user', 'user_id', 'zone'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |