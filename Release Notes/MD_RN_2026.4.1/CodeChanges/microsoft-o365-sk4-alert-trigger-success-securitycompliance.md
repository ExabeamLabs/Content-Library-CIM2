# Code Changes for microsoft-o365-sk4-alert-trigger-success-securitycompliance (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'app', 'category', 'email_address', 'malware_url', 'operation', 'result', 'tenant_id', 'time'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"?({tenant_id}[^\s,=.<"]+)'] |