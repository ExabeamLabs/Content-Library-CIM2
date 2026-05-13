# Code Changes for microsoft-o365-sk4-file-app-userkey-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'object', 'object_id', 'object_type', 'operation', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_agent', 'user_type'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |