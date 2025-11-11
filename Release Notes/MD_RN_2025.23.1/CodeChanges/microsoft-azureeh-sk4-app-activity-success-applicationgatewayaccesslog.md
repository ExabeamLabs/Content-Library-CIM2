# Code Changes for microsoft-azureeh-sk4-app-activity-success-applicationgatewayaccesslog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'bytes_in', 'bytes_out', 'category', 'cipher', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'event_name', 'host', 'instance_id', 'method', 'object', 'operation', 'policy_content', 'protocol', 'provider_name', 'query', 'resource_group', 'resource_id', 'result', 'result_code', 'router_ip_flow', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'tunnel_protocol', 'uri', 'user', 'user_agent', 'vm_pool_name', 'web_domain'] |
| edit_regex_field | operation |  | ['([^\|]*\|){5}({event_name}({operation}[^\|]+))', '\Wact=({event_name}({operation}[^=]+))\s+(\w+=|$)', '\WflexString1=({event_name}({operation}[^=]+))\s+(\w+=|$)', 'operationName":"({event_name}({operation}.+?[^\\]))"'] |
| added_regex_field | event_name |  | ['([^\|]*\|){5}({event_name}({operation}[^\|]+))', '\Wact=({event_name}({operation}[^=]+))\s+(\w+=|$)', '\WflexString1=({event_name}({operation}[^=]+))\s+(\w+=|$)', 'operationName":"({event_name}({operation}.+?[^\\]))"'] |
| removed_attribute | DupFields |  | N/A |