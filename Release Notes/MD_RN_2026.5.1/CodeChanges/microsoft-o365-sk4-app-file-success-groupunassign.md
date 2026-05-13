# Code Changes for microsoft-o365-sk4-app-file-success-groupunassign (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'connection_id', 'email_address', 'email_domain', 'event_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'resource', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_agent'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |