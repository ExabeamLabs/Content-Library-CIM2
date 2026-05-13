# Code Changes for microsoft-evsecurity-sk4-user-create-success-usercreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'category', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'full_name', 'login_id', 'tenant_id', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | tenant_id |  | ['"TenantId":"({tenant_id}[^"]+)'] |