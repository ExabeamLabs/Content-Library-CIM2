# Code Changes for microsoft-defenderep-json-endpoint-notification-deviceinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['device_id', 'domain', 'event_name', 'host', 'os', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |