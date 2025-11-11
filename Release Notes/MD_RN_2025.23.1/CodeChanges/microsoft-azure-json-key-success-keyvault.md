# Code Changes for microsoft-azure-json-key-success-keyvault (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'correlation_id', 'creds_name', 'creds_path', 'email_address', 'email_domain', 'event_category', 'failure_reason', 'http_response_code', 'key_type', 'operation', 'operation_name', 'operation_type', 'operation_version', 'resource', 'resource_group', 'resource_id', 'resource_name', 'resource_path', 'resource_type', 'result_code', 'service_name', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'url', 'user_agent'] |
| edit_regex_field | operation |  | ['"+OperationName"+:\s*"+({operation_name}({operation}[^"]+))"+'] |
| added_regex_field | operation_name |  | ['"+OperationName"+:\s*"+({operation_name}({operation}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |