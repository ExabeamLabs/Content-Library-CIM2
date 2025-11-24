# Code Changes for microsoft-azuremon-sk4-app-activity-applicationgatewayaccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes_in', 'bytes_out', 'category', 'dest_ip', 'dest_port', 'email_address', 'event_name', 'method', 'object', 'operation', 'resource_id', 'result', 'result_code', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'uri', 'user', 'user_agent'] |
| edit_regex_field | operation |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |