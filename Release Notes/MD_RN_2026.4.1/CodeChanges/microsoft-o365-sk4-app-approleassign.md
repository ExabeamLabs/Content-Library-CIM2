# Code Changes for microsoft-o365-sk4-app-approleassign (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'app', 'browser', 'correlation_id', 'dest_domain', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'host', 'object', 'operation', 'os', 'resource', 'result', 'role_name', 'src_host', 'src_ip', 'src_port', 'target', 'tenant_id', 'time', 'user', 'user_agent', 'user_type', 'user_upn'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"?({tenant_id}[^\s,=.<"]+)'] |