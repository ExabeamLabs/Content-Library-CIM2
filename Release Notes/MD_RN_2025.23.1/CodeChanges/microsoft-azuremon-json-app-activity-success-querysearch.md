# Code Changes for microsoft-azuremon-json-app-activity-success-querysearch (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'duration', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'operation', 'query', 'resource', 'resource_group', 'resource_id', 'server_group', 'server_name', 'src_ip', 'src_port', 'subscription_id', 'time', 'user'] |
| edit_regex_field | action |  | ['"event_subclass":"({operation}({action}[^",]+))', '"operationName":"({operation}({action}[^"]+))'] |
| edit_regex_field | event_hub_name |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)', 'exa_regex=EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]'] |
| edit_regex_field | event_hub_namespace |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)', 'exa_regex=Namespace:\s*(|({host}({event_hub_namespace}[^\]]+?)))\s*[\];]'] |
| edit_regex_field | resource |  | ['"resourceId":"({object}({resource}[^",]+))'] |
| added_regex_field | host |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)', 'exa_regex=Namespace:\s*(|({host}({event_hub_namespace}[^\]]+?)))\s*[\];]'] |
| added_regex_field | object |  | ['"resourceId":"({object}({resource}[^",]+))'] |
| added_regex_field | operation |  | ['"event_subclass":"({operation}({action}[^",]+))', '"operationName":"({operation}({action}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |