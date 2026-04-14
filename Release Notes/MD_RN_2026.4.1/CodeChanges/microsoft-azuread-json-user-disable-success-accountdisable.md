# Code Changes for microsoft-azuread-json-user-disable-success-accountdisable (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'category', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_name', 'operation', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_sid', 'user_uid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |