# Code Changes for unix-unix-str-endpoint-login-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_method', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'failure_reason', 'host', 'process_id', 'process_name', 'result', 'time', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |