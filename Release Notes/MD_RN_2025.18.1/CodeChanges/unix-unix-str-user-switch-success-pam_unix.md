# Code Changes for unix-unix-str-user-switch-success-pam_unix (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_user', 'dest_user_id', 'email_address', 'event_code', 'event_name', 'host', 'src_ip', 'src_port', 'time', 'user', 'user_id', 'user_uid'] |
| added_regex_field | event_name |  | ['({event_name}session opened)'] |