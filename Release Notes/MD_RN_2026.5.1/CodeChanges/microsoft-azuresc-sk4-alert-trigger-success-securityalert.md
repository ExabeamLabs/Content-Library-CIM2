# Code Changes for microsoft-azuresc-sk4-alert-trigger-success-securityalert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'location_city', 'location_country', 'malware_url', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |