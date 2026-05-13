# Code Changes for cef-azure-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_address', 'incident_status', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"'] |