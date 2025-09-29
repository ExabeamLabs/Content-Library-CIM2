# Code Changes for unix-unix-str-endpoint-login-fail-invaliduser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'email_address', 'event_code', 'failure_reason', 'host', 'login_id', 'process_id', 'process_name', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |