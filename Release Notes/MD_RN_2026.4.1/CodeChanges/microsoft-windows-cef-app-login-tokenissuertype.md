# Code Changes for microsoft-windows-cef-app-login-tokenissuertype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'auth_method', 'browser', 'category', 'country_code', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_code', 'failure_reason', 'first_name', 'full_name', 'last_name', 'os', 'resource', 'result', 'severity', 'src_host', 'src_ip', 'tenant_id', 'time', 'user_agent', 'user_id'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |