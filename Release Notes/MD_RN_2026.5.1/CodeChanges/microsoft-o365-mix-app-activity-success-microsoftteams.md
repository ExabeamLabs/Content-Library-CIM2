# Code Changes for microsoft-o365-mix-app-activity-success-microsoftteams (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'app', 'email_address', 'email_domain', 'object', 'operation', 'src_ip', 'tenant_id', 'time', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"ResourceTenantId":\s*"({tenant_id}[^"]+)'] |