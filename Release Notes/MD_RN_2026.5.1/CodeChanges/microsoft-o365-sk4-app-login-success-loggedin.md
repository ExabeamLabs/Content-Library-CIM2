# Code Changes for microsoft-o365-sk4-app-login-success-loggedin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'browser', 'country_code', 'email_address', 'email_domain', 'full_name', 'location_city', 'location_state', 'os', 'result', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"resourceTenantId":\s*"({tenant_id}[^"]+)"'] |