# Code Changes for microsoft-azuremon-json-database-activity-success-querystoreruntimestatistics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'db_name', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'operation', 'resource', 'resource_group', 'resource_id', 'server_group', 'server_name', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |