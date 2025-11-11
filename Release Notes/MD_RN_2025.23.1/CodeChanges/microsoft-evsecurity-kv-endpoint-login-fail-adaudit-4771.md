# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'failure_code', 'host', 'result', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_code |  | ['ERROR_CODE\s*=\s*({failure_code}({result_code}[^\s]+))'] |
| added_regex_field | failure_code |  | ['ERROR_CODE\s*=\s*({failure_code}({result_code}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |