# Code Changes for microsoft-o365-cef-app-file-success-fileupload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'browser', 'bytes', 'category', 'correlation_id', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'email_address', 'email_domain', 'email_subject', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'file_url', 'first_name', 'full_name', 'group_name', 'hash_sha256', 'host', 'key_name', 'last_name', 'object', 'operation', 'operation_type', 'os', 'printer_name', 'process_name', 'resource', 'resource_id', 'result', 'result_code', 'rule', 'secret', 'service_name', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id', 'user_sid', 'user_type'] |
| removed_regex_field | src_file_path |  | [] |
| added_regex_field | app_id |  | ['appId":"({app_id}[^"]+)"'] |
| added_regex_field | src_file_dir |  | ['"SourceRelativeUrl":"({src_file_dir}[^"]+)"'] |