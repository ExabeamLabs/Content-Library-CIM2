# Code Changes for unix-unix-kv-database-login-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'email_address', 'event_name', 'host', 'process_id', 'process_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_id'] |
| edit_regex_field | process_id |  | ['({host}[\w\.\-]+)?:?\s*journal\s*\[({process_id}[^\]]+)\]', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |