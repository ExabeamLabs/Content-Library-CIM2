# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4648 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'auth_package', 'dest_host', 'dest_ip', 'dest_port', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'result', 'result_code', 'service_name', 'src_external_country', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['"user":\{[^\}]*?"uid":"({account}({dest_user}[^"]+))'] |
| added_regex_field | account |  | ['"user":\{[^\}]*?"uid":"({account}({dest_user}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |