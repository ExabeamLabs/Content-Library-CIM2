# Code Changes for microsoft-evsecurity-json-endpoint-notification-5033 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"TenantId"\s*:\s*"({tenant_id}[^"]+)"'] |