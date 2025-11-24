# Code Changes for microsoft-azuremon-sk4-app-notification-gatewaylogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'bytes_in', 'bytes_out', 'category', 'email_address', 'event_name', 'failure_reason', 'http_response_code', 'method', 'operation', 'protocol', 'resource_id', 'result', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'url', 'user', 'web_domain'] |
| edit_regex_field | operation |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |