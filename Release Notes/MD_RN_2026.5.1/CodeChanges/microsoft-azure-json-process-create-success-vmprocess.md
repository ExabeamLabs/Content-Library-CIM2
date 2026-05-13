# Code Changes for microsoft-azure-json-process-create-success-vmprocess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'host', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_host', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |