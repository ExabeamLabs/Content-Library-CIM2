# Code Changes for microsoft-azuread-sk4-user-password-modify-success-changepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'category', 'dest_email_address', 'dest_email_domain', 'dest_user', 'dest_user_full_name', 'email_address', 'event_name', 'operation', 'result', 'tenant_id', 'time'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"'] |