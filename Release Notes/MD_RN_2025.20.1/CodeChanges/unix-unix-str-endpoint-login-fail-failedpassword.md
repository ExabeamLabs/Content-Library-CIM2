# Code Changes for unix-unix-str-endpoint-login-fail-failedpassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'event_code', 'failure_reason', 'host', 'host_ip', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |