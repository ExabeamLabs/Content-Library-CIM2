# Code Changes for microsoft-m365auditlogs-json-app-activity-operationname (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'app', 'attribute', 'category', 'correlation_id', 'email_address', 'email_domain', 'error_code', 'host', 'object', 'operation', 'principal_id', 'result', 'result_reason', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_uid'] | ['additional_info', 'app', 'attribute', 'category', 'correlation_id', 'dest_host', 'email_address', 'email_domain', 'error_code', 'host', 'object', 'operation', 'principal_id', 'result', 'result_reason', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_uid'] |
| added_regex_field | dest_host | [] | ['"targetResources":.+?"displayName":"({dest_host}[\w\-.]+)"'] |