# Code Changes for microsoft-azuresc-json-alert-trigger-success-anomalouspageaccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_name', 'full_name', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_upn'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"'] |