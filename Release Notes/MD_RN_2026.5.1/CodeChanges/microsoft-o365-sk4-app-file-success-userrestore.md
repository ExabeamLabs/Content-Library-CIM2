# Code Changes for microsoft-o365-sk4-app-file-success-userrestore (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'connection_id', 'email_address', 'email_domain', 'event_name', 'log_source', 'object_id', 'object_type', 'operation', 'os', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |