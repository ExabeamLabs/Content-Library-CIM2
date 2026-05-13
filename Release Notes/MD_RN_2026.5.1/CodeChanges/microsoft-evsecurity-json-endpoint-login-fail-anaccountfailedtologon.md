# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-anaccountfailedtologon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_reason', 'host', 'login_type', 'result_reason', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| removed_regex_field | result_code |  | [] |
| added_regex_field | result_reason |  | ['"Sub_Status":"({result_reason}[^"]+)'] |