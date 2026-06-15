# Code Changes for delinea-centrifyztps-kv-user-switch-success-granted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_user', 'domain', 'event_name', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'service_name', 'time', 'user'] |
| removed_regex_field | object |  | [] |
| added_regex_field | dest_host |  | ['EntityName=({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)'] |
| added_regex_field | domain |  | ['EntityName=({domain}[^\\]+)\\+({dest_host}[\w\-\.]+)'] |