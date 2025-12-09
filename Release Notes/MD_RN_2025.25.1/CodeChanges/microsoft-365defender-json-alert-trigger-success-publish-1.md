# Code Changes for microsoft-365defender-json-alert-trigger-success-publish-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'host', 'tenant_id', 'time'] |
| added_regex_field | tenant_id |  | ['"tenantId":"({tenant_id}[^"]+)"'] |