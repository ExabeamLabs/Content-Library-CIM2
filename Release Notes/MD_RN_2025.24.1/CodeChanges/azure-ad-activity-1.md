# Code Changes for azure-ad-activity-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'email_address', 'event_name', 'operation', 'resource_id', 'result', 'src_host', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'user'] |
| edit_regex_field | operation |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"OperationName":\s*"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |