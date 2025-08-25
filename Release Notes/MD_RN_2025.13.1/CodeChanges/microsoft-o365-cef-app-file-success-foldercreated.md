# Code Changes for microsoft-o365-cef-app-file-success-foldercreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'browser', 'category', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'email_address', 'email_domain', 'email_subject', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'group_name', 'host', 'key_name', 'last_name', 'object', 'operation', 'operation_type', 'os', 'process_name', 'resource', 'resource_id', 'result', 'secret', 'service_name', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id', 'user_sid', 'user_type'] |
| added_regex_field | app_id |  | ['appId":"({app_id}[^"]+)"'] |