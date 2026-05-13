# Code Changes for microsoft-azuread-cef-app-login-signinoperation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'app', 'category', 'email_address', 'error_code', 'event_name', 'failure_reason', 'object', 'operation', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_agent', 'user_uid'] |
| added_regex_field | tenant_id |  | ['"TenantId":"({tenant_id}[^"]+)"'] |