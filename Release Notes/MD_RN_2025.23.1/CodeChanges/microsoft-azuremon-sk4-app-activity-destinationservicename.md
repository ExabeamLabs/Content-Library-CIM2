# Code Changes for microsoft-azuremon-sk4-app-activity-destinationservicename (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_server', 'category', 'correlation_id', 'duration', 'email_address', 'event_hub_name', 'event_hub_namespace', 'event_name', 'hash_md5', 'hash_sha256', 'host', 'mime', 'object', 'object_type', 'operation', 'os', 'provider_name', 'region', 'repository_name', 'resource', 'resource_group', 'resource_id', 'result_code', 'src_ip', 'src_port', 'subscription_id', 'tag', 'tenant_id', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['"operationName":"({event_name}({operation}[^",]+))', '({event_name}ContainerRegistryRepositoryEvents)'] |
| edit_regex_field | operation |  | ['"operationName":"({event_name}({operation}[^",]+))'] |
| edit_regex_field | repository_name |  | ['"repository":\s*"({object}({repository_name}[^"]+))"'] |
| added_regex_field | object |  | ['"repository":\s*"({object}({repository_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |