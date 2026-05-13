# Code Changes for microsoft-evsecurity-csv-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'computer_name', 'dest_host', 'domain', 'event_code', 'failure_code', 'host', 'login_type', 'result_code', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | result_code |  | ['サブ ステータス:\s+({failure_code}({result_code}[^\s]+)) '] |
| added_regex_field | failure_code |  | ['サブ ステータス:\s+({failure_code}({result_code}[^\s]+)) '] |