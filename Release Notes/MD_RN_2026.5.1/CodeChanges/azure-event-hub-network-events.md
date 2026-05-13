# Code Changes for azure-event-hub-network-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_name', 'host', 'process_id', 'protocol', 'src_ip', 'src_port', 'tenant_id', 'time', 'url', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |