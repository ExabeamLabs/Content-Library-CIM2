# Code Changes for microsoft-m365auditlogs-json-app-activity-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'email_address', 'event_name', 'object_id', 'object_type', 'operation', 'resource', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user'] |
| added_regex_field | tenant_id |  | ['(?i:tenantid)":"({tenant_id}[^"]+)'] |