# Code Changes for microsoft-o365-mix-file-success-workload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'action', 'app', 'auth_method', 'browser', 'bytes', 'correlation_id', 'dest_email_address', 'dest_user', 'domain', 'email_address', 'email_domain', 'external_id', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_permissions', 'file_type', 'file_url', 'full_name', 'host', 'new_attribute', 'old_sensitivity_label', 'operation', 'operation_details', 'resource_name', 'resource_type', 'sensitivity_label', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'tag', 'time', 'url', 'user', 'user_agent', 'user_id', 'user_type', 'web_domain'] |
| added_regex_field | resource_name |  | ['"ListName":"({resource_name}[^"]+)"'] |
| added_regex_field | resource_type |  | ['"ListBaseType":"({resource_type}[^"]+)"'] |