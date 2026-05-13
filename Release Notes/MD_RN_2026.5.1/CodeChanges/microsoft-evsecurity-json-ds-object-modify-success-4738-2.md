# Code Changes for microsoft-evsecurity-json-ds-object-modify-success-4738-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'login_id', 'src_domain', 'src_user', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"TenantId"\s*:\s*"({tenant_id}[^"]+)"'] |