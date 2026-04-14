# Code Changes for microsoft-azuremon-json-file-storagecategory (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'correlation_id', 'file_ext', 'file_name', 'file_path', 'location', 'operation', 'protocol', 'region', 'resource_id', 'resource_type', 'result', 'result_code', 'service_name', 'service_type', 'src_ip', 'src_port', 'storage_account', 'tenant_id', 'time', 'url', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |