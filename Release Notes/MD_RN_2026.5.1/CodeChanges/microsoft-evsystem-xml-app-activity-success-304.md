# Code Changes for microsoft-evsystem-xml-app-activity-success-304 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'event_name', 'host', 'process_id', 'run_level', 'tenant_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
| added_regex_field | tenant_id |  | ['"TenantId":"({tenant_id}[^"]+)'] |