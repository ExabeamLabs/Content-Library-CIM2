# Code Changes for microsoft-azure-json-app-activity-addgroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_category', 'event_name', 'group_name', 'group_type', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result', 'src_ip', 'src_port', 'subscription_id', 'target', 'tenant_id', 'time', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |