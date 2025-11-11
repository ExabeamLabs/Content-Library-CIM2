# Code Changes for microsoft-azure-json-file-success-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_type', 'bytes_in', 'bytes_out', 'correlation_id', 'dest_host', 'email_address', 'email_domain', 'event_category', 'file_modify_time', 'file_name', 'file_path', 'operation', 'operation_name', 'operation_type', 'operation_version', 'protocol', 'referrer', 'region', 'resource_id', 'result', 'result_code', 'schema_version', 'src_ip', 'src_port', 'storage_account', 'subscription_id', 'tenant_id', 'time', 'url', 'user_agent'] |
| edit_regex_field | operation |  | ['"+OperationName"+:\s*"+({operation_name}({operation}[^"]+))"+'] |
| edit_regex_field | storage_account |  | ['"+AccountName"+:\s*"+({dest_host}({storage_account}[^"]+))"+'] |
| added_regex_field | dest_host |  | ['"+AccountName"+:\s*"+({dest_host}({storage_account}[^"]+))"+'] |
| added_regex_field | operation_name |  | ['"+OperationName"+:\s*"+({operation_name}({operation}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |