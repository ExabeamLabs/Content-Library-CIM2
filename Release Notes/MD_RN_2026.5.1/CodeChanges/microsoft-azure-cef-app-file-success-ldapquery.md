# Code Changes for microsoft-azure-cef-app-file-success-ldapquery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'app', 'attack_info', 'category', 'dest_host', 'dest_ip', 'dest_port', 'dest_user_sid', 'email_address', 'email_domain', 'first_name', 'full_name', 'group_name', 'host', 'last_name', 'operation', 'os', 'process_guid', 'protocol', 'result', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | tenant_id |  | ['"aadTenantId":\s*"({tenant_id}[^"]+)"', '"tenantId":\s*"({tenant_id}[^"]+)"'] |