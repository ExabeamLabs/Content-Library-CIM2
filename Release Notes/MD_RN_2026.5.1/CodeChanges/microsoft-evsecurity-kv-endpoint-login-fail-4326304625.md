# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4326304625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'login_type', 'result_code', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | result_code |  | ['nitroMessage_Text=({result_code}({failure_code}[^\s]+))\s+\w+='] |
| added_regex_field | failure_code |  | ['nitroMessage_Text=({result_code}({failure_code}[^\s]+))\s+\w+='] |