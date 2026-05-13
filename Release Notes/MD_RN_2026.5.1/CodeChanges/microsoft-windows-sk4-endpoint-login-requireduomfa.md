# Code Changes for microsoft-windows-sk4-endpoint-login-requireduomfa (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'category', 'city', 'country', 'db_name', 'dest_host', 'email_address', 'email_domain', 'full_name', 'resource', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_agent', 'user_id'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |