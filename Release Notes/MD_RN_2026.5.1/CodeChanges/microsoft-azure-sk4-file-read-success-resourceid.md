# Code Changes for microsoft-azure-sk4-file-read-success-resourceid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'object', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |