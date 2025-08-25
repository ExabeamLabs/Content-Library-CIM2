# Code Changes for microsoft-windows-sk4-app-login-fail-signin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'attribute', 'auth_method', 'browser', 'category', 'city', 'country_code', 'device_id', 'email_address', 'email_domain', 'error_code', 'failure_code', 'failure_reason', 'first_name', 'full_name', 'last_name', 'location', 'operation', 'os', 'principal_id', 'resource', 'result', 'severity', 'src_host', 'src_ip', 'src_port', 'state', 'time', 'user_agent', 'user_id'] |
| added_regex_field | attribute |  | ['servicePrincipalName":"({attribute}[^",]+)"'] |
| added_regex_field | principal_id |  | ['"servicePrincipalId":\s*"({principal_id}[^"]+)"'] |