# Code Changes for unix-unix-kv-endpoint-login-sshdauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'process_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_id'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |