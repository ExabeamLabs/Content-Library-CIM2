# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'failure_code', 'host', 'login_type_text', 'result_code', 'src_host', 'time', 'user', 'user_upn'] |
| edit_regex_field | result_code |  | ['Error Code:\s*({failure_code}({result_code}[^\s"]+))\s*"?'] |
| added_regex_field | failure_code |  | ['Error Code:\s*({failure_code}({result_code}[^\s"]+))\s*"?'] |
| removed_attribute | DupFields |  | N/A |