# Code Changes for microsoft-azureadsignin-cef-app-login-success-signin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'email_address', 'event_name', 'first_name', 'full_name', 'last_name', 'operation', 'src_ip', 'tenant_id', 'time', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |