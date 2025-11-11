# Code Changes for microsoft-evsecurity-csv-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'computer_name', 'dest_host', 'domain', 'event_code', 'host', 'login_type', 'result_code', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | host |  | ['(?!\d+)({dest_host}({host}[\w\-.]+)),([^,]*,)?アカウントがログオンに失敗しました。', 'ComputerName=({host}[\w.\-]+)'] |
| added_regex_field | dest_host |  | ['(?!\d+)({dest_host}({host}[\w\-.]+)),([^,]*,)?アカウントがログオンに失敗しました。', 'ComputerName=({dest_host}[\w.\-]+)'] |
| removed_attribute | DupFields |  | N/A |