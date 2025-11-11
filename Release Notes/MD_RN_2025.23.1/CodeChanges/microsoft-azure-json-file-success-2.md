# Code Changes for microsoft-azure-json-file-success-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_type', 'bytes_in', 'bytes_out', 'category', 'correlation_id', 'file_modify_time', 'file_name', 'file_path', 'location', 'operation', 'operation_name', 'operation_type', 'operation_version', 'protocol', 'region', 'resource', 'resource_type', 'result', 'result_code', 'schema_version', 'service_name', 'service_type', 'src_ip', 'src_port', 'storage_account', 'time', 'url', 'user_agent', 'user_upn'] |
| edit_regex_field | operation |  | ['"+operationName"+:\s*"+({operation_name}({operation}[^"]+))"+'] |
| edit_regex_field | operation_type |  | ['"+category"+:\s*"+({category}({operation_type}[^"]+))"+'] |
| edit_regex_field | region |  | ['"+location"+:\s*"+({location}({region}[^"]+))"+'] |
| added_regex_field | category |  | ['"+category"+:\s*"+({category}({operation_type}[^"]+))"+'] |
| added_regex_field | location |  | ['"+location"+:\s*"+({location}({region}[^"]+))"+'] |
| added_regex_field | operation_name |  | ['"+operationName"+:\s*"+({operation_name}({operation}[^"]+))"+'] |
| removed_attribute | DupFields |  | N/A |