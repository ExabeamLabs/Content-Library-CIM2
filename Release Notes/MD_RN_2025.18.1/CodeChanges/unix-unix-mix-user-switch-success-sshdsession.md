# Code Changes for unix-unix-mix-user-switch-success-sshdsession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_user_id', 'event_code', 'event_name', 'host', 'login_id', 'project_id', 'time', 'user', 'user_id', 'zone'] |
| added_regex_field | event_name |  | ['({event_name}session opened)'] |