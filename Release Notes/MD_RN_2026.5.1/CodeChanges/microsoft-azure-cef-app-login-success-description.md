# Code Changes for microsoft-azure-cef-app-login-success-description (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'browser', 'country_code', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'error_code', 'event_name', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'os', 'protocol', 'result', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_agent', 'user_id'] |
| added_regex_field | tenant_id |  | ['"aadTenantId":\s*"({tenant_id}[^"]+)"', '"tenantId":\s*"({tenant_id}[^"]+)"'] |