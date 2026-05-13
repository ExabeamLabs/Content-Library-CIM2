# Code Changes for microsoft-evadfs-sk4-app-notification-success-431 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'host', 'log_source', 'login_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |