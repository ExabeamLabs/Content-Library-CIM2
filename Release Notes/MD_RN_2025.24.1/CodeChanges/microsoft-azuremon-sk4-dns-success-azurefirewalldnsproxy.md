# Code Changes for microsoft-azuremon-sk4-dns-success-azurefirewalldnsproxy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'category', 'event_name', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'rule_source', 'rule_type', 'subscription_id', 'time'] |
| edit_regex_field | operation |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"operationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |