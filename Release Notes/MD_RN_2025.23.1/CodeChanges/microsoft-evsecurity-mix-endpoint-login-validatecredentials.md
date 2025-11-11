# Code Changes for microsoft-evsecurity-mix-endpoint-login-validatecredentials (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'failure_code', 'host', 'login_type_text', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| edit_regex_field | result_code |  | ['Error Code(:|=)\s*({failure_code}({result_code}[\w\-]+))'] |
| added_regex_field | failure_code |  | ['Error Code(:|=)\s*({failure_code}({result_code}[\w\-]+))'] |
| removed_attribute | DupFields |  | N/A |