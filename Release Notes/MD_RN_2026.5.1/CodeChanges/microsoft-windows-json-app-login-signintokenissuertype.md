# Code Changes for microsoft-windows-json-app-login-signintokenissuertype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_method', 'category', 'country_code', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_reason', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'result', 'severity', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_agent', 'user_uid'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |