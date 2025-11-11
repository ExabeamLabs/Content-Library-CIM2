# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4624-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'host', 'login_id', 'login_type', 'process_path', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(?!\d+)({dest_host}({host}[\w\-.]+)),([^,]*,)?アカウントが正常にログオンしました。', 'ComputerName=({dest_host}({host}[\w.\-]+))'] |
| added_regex_field | dest_host |  | ['(?!\d+)({dest_host}({host}[\w\-.]+)),([^,]*,)?アカウントが正常にログオンしました。', 'ComputerName=({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |