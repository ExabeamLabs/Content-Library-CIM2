# Code Changes for microsoft-defenderep-sk4-alert-trigger-success-securityalerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'hash_sha1', 'host', 'incident_status', 'src_ip', 'src_port', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |