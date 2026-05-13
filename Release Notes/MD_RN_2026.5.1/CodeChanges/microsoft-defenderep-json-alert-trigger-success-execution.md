# Code Changes for microsoft-defenderep-json-alert-trigger-success-execution (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_name', 'full_name', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_upn'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |