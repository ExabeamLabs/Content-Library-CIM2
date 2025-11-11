# Code Changes for microsoft-windows-sk4-app-login-fail-signin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'attribute', 'auth_method', 'browser', 'category', 'city', 'country_code', 'device_id', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_code', 'failure_reason', 'first_name', 'full_name', 'last_name', 'location', 'operation', 'os', 'principal_id', 'resource', 'result', 'severity', 'src_host', 'src_ip', 'src_port', 'state', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | operation |  | ['"+operationName"+:"+({event_name}({operation}[^"]+))"+', 'exa_regex="+operationName"+:"+({event_name}({operation}[^"]+))"+'] |
| added_regex_field | event_name |  | ['"+operationName"+:"+({event_name}({operation}[^"]+))"+', 'exa_regex="+operationName"+:"+({event_name}({operation}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |