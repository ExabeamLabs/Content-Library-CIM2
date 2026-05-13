# Code Changes for cef-azure-audit (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'event_category', 'event_name', 'object', 'operation', 'resource', 'resource_id', 'src_ip', 'tenant_id', 'time'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |