# Code Changes for microsoft-azure-cef-group-member-remove-success-removefromgroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'app', 'email_address', 'email_domain', 'event_name', 'group_name', 'operation', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_uid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |