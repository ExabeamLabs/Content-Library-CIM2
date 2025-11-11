# Code Changes for microsoft-azuremon-sk4-http-request-frontdoorwebapplicationfirewalllog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_type', 'app', 'category', 'dest_host', 'event_hub_name', 'event_hub_namespace', 'host', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'src_ip', 'src_port', 'subscription_id', 'time', 'url', 'user'] |
| edit_regex_field | event_hub_namespace |  | ['Namespace:\s*({host}({event_hub_namespace}\S+))'] |
| edit_regex_field | host |  | ['"host":"({host}[^"]+)', 'Namespace:\s*({host}({event_hub_namespace}\S+))'] |
| edit_regex_field | object |  | ['"resourceId":"({resource}({object}[^"]+))'] |
| added_regex_field | resource |  | ['"resourceId":"({resource}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |