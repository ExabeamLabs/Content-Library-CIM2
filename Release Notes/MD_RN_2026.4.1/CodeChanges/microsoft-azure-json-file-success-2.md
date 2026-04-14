# Code Changes for microsoft-azure-json-file-success-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_type', 'bytes_in', 'bytes_out', 'category', 'correlation_id', 'file_modify_time', 'file_name', 'file_path', 'location', 'operation', 'operation_name', 'operation_type', 'operation_version', 'protocol', 'region', 'resource', 'resource_type', 'result', 'result_code', 'schema_version', 'service_name', 'service_type', 'src_ip', 'src_port', 'storage_account', 'tenant_id', 'time', 'url', 'user_agent', 'user_upn'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |