# Code Changes for microsoft-defenderep-sk4-alert-trigger-success-windowsdefenderav (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'host', 'incident_status', 'result', 'src_ip', 'src_port', 'technique', 'tenant_id', 'time'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |