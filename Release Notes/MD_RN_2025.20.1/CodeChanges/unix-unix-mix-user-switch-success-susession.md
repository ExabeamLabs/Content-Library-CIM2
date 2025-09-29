# Code Changes for unix-unix-mix-user-switch-success-susession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_user', 'dest_user_id', 'event_code', 'event_name', 'host', 'process_id', 'process_name', 'time', 'user', 'user_uid'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |