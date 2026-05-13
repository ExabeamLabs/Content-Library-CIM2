# Code Changes for microsoft-m365auditlogs-json-app-activity-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'app', 'attribute', 'category', 'correlation_id', 'device_name', 'email_address', 'email_domain', 'error_code', 'full_name', 'host', 'object', 'operation', 'principal_id', 'result', 'result_reason', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_uid'] |
| removed_regex_field | dest_host |  | [] |
| added_regex_field | device_name |  | ['"targetResources":.+?"displayName":"({device_name}[\w\-.][^"]+)".+?"type":"Device"'] |