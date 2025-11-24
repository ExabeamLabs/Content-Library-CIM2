# Code Changes for microsoft-azuremon-sk4-app-activity-success-virtualnetworkgateways (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'category', 'email_address', 'event_name', 'operation', 'resource_id', 'result', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'user'] |
| edit_regex_field | operation |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |