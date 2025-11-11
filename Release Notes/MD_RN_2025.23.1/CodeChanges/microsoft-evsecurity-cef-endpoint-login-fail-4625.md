# Code Changes for microsoft-evsecurity-cef-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'key_length', 'location', 'login_type', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | host |  | ['\sdvc=({dest_host}({host}[a-fA-F:\d.]+))', '\sdvchost=({dest_host}({host}[^\s]+))'] |
| edit_regex_field | result_code |  | ['Account locked out.+?flexString1=({failure_code}({result_code}[^\s]+))', 'Sub_,Status=({failure_code}({result_code}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\sdvc=({dest_host}({host}[a-fA-F:\d.]+))', '\sdvchost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | failure_code |  | ['Account locked out.+?flexString1=({failure_code}({result_code}[^\s]+))', 'Sub_,Status=({failure_code}({result_code}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |