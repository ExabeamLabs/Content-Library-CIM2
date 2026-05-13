# Code Changes for microsoft-evsecurity-sk4-share-create-success-5142 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'share_name', 'share_path', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"TenantId":"({tenant_id}[^"]+)'] |