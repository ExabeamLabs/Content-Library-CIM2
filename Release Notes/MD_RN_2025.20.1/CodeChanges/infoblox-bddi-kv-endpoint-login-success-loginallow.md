# Code Changes for infoblox-bddi-kv-endpoint-login-success-loginallow (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'auth_method', 'event_name', 'group_name', 'host', 'process_id', 'process_name', 'src_ip', 'src_port', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |