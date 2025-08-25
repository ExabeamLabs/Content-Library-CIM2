# Code Changes for microsoft-m365auditlogs-json-app-activity-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'attribute', 'category', 'correlation_id', 'email_address', 'email_domain', 'error_code', 'host', 'object', 'operation', 'principal_id', 'result', 'result_reason', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_uid'] |
| added_regex_field | attribute |  | ['servicePrincipalName":"({attribute}[^",]+)"'] |
| added_regex_field | principal_id |  | ['"servicePrincipalId":\s*"(null|({principal_id}[^"]+))"'] |