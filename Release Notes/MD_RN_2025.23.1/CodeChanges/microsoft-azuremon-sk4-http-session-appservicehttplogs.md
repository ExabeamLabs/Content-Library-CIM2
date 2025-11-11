# Code Changes for microsoft-azuremon-sk4-http-session-appservicehttplogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'browser', 'bytes_in', 'bytes_out', 'category', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'host', 'http_response_code', 'method', 'operation', 'os', 'referrer', 'resource', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | app |  | ['"CsHost\\?":\\?"({web_domain}({app}[^:",]+?))\\?"', 'destinationServiceName=({web_domain}({app}.+?))\s+(\w+=|$)'] |
| edit_regex_field | event_hub_name |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| edit_regex_field | event_hub_namespace |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| added_regex_field | host |  | ['\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)'] |
| added_regex_field | web_domain |  | ['"CsHost\\?":\\?"({web_domain}({app}[^:",]+?))\\?"', 'destinationServiceName=({web_domain}({app}.+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |