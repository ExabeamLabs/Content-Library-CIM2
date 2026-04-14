# Code Changes for microsoft-azure-cef-app-login-success-auditlogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'email_address', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'operation', 'protocol', 'resource_id', 'result', 'src_ip', 'subscription_id', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |