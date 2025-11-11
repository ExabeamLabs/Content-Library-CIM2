# Code Changes for microsoft-azuremon-sk4-app-activity-success-containerservice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'container_id', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'role', 'service_name', 'src_ip', 'src_port', 'subscription_id', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_hub_name |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| edit_regex_field | event_hub_namespace |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| added_regex_field | host |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| removed_attribute | DupFields |  | N/A |