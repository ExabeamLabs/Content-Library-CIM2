# Code Changes for sentinelone-singularityp-json-endpoint-login-success-logins (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'domain', 'email_address', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'host_type', 'operation_type', 'os', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | result |  | ['event.login.loginIsSuccessful":"({result}[^"]+)'] |