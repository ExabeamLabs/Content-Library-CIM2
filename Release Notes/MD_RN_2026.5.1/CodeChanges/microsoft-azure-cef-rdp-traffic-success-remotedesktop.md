# Code Changes for microsoft-azure-cef-rdp-traffic-success-remotedesktop (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'protocol', 'result', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"aadTenantId":\s*"({tenant_id}[^"]+)"', '"tenantId":\s*"({tenant_id}[^"]+)"'] |