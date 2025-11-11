# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-authfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'result_code', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_code |  | ['Failure Code:\s*({failure_code}({result_code}[\w]+))'] |
| added_regex_field | failure_code |  | ['Failure Code:\s*({failure_code}({result_code}[\w]+))'] |
| removed_attribute | DupFields |  | N/A |