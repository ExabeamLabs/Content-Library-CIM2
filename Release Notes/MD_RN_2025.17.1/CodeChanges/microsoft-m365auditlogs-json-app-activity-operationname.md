# Code Changes for microsoft-m365auditlogs-json-app-activity-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'app', 'attribute', 'category', 'correlation_id', 'dest_host', 'email_address', 'email_domain', 'error_code', 'full_name', 'host', 'object', 'operation', 'principal_id', 'result', 'result_reason', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_uid'] |
| edit_regex_field | app |  | ['"?loggedByService":\s*"(?:Account Provisioning|Core Directory|({app}[^",]+))"?', '"app":\{[^\}]+?displayName":"({app}[^",]+)', '"category":"(?!RiskyUsers|UserRiskEvents|ProvisioningLogs)[^"]+"[^=]+?"identity":"({app}[^"]+)"', '"identity":"({app}[^"]+)"[^=]+?"category":"(?!RiskyUsers|UserRiskEvents|ProvisioningLogs)[^"]+"'] |
| added_regex_field | alert_severity |  | ['"riskLevel":"(none|({alert_severity}[^"]+))"'] |