# Code Changes for microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'dest_ip', 'dest_port', 'event_name', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'src_ip', 'src_port', 'subscription_id', 'time', 'web_domain'] |
| edit_regex_field | operation |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |