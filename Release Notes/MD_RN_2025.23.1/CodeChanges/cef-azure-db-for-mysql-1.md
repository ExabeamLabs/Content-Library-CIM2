# Code Changes for cef-azure-db-for-mysql-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'event_hub_name', 'event_hub_namespace', 'host', 'operation', 'resource_group', 'resource_id', 'server_name', 'src_ip', 'src_port', 'subscription_id', 'time', 'user'] |
| edit_regex_field | action |  | ['"event_subclass":"({operation}({action}[^",]+))', '"operationName":"({operation}({action}[^"]+))'] |
| edit_regex_field | event_hub_name |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| edit_regex_field | event_hub_namespace |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| added_regex_field | host |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| added_regex_field | operation |  | ['"event_subclass":"({operation}({action}[^",]+))', '"operationName":"({operation}({action}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |