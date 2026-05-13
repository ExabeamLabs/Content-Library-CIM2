# Code Changes for microsoft-evsecurity-xml-policy-modify-5447-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'layer_name', 'process_id', 'run_level', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
| added_regex_field | tenant_id |  | ['"TenantId":"({tenant_id}[^"]+)'] |