# Code Changes for microsoft-azuremon-sk4-http-session-frontdooraccesslog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'browser', 'bytes_in', 'bytes_out', 'category', 'event_hub_name', 'event_hub_namespace', 'host', 'http_response_code', 'method', 'object', 'operation', 'os', 'protocol', 'provider_name', 'resource', 'resource_group', 'resource_id', 'src_ip', 'src_port', 'subscription_id', 'time', 'uri_path', 'uri_query', 'url', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | event_hub_namespace |  | ['Namespace:\s*({host}({event_hub_namespace}\S+))'] |
| edit_regex_field | host |  | ['"backendHostname":"({host}[^:"]+)', 'Namespace:\s*({host}({event_hub_namespace}\S+))'] |
| edit_regex_field | object |  | ['"resourceId":"({resource}({object}[^"]+))'] |
| added_regex_field | resource |  | ['"resourceId":"({resource}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |