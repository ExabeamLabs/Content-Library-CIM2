# Code Changes for microsoft-o365-sk4-app-activity-success-sentmailbox (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_domain', 'domain', 'email_address', 'email_domain', 'host', 'object_id', 'operation', 'policy_name', 'result', 'src_ip', 'src_port', 'target', 'tenant_id', 'time', 'user', 'user_type'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"?({tenant_id}[^\s,=.<"]+)'] |