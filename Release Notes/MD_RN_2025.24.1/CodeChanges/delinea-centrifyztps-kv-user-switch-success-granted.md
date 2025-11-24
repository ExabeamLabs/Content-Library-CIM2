# Code Changes for delinea-centrifyztps-kv-user-switch-success-granted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_user', 'event_name', 'host', 'object', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'service_name', 'time', 'user'] |
| edit_regex_field | dest_user |  | ['runas=({account}({dest_user}.+?))\s\w+='] |
| added_regex_field | account |  | ['runas=({account}({dest_user}.+?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |