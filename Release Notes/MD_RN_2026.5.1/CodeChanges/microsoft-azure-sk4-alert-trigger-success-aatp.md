# Code Changes for microsoft-azure-sk4-alert-trigger-success-aatp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_user', 'full_name', 'host', 'incident_status', 'malware_url', 'src_host', 'src_ip', 'src_location', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":"({tenant_id}[^",]+)'] |