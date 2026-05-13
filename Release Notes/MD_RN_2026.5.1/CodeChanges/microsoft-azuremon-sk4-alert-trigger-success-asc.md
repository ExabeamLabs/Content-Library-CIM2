# Code Changes for microsoft-azuremon-sk4-alert-trigger-success-asc (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'event_name', 'host', 'src_ip', 'src_port', 'tenant_id', 'time'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"'] |