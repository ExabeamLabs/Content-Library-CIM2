# Code Changes for microsoft-azuread-json-group-member-add-success-aadiam (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'app', 'category', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_name', 'group_id', 'group_name', 'member', 'operation', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_uid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |