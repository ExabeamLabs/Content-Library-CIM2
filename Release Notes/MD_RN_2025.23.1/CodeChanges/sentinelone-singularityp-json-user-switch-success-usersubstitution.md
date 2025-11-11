# Code Changes for sentinelone-singularityp-json-user-switch-success-usersubstitution (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'alert_severity', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'device_type', 'domain', 'email_address', 'email_domain', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'full_name', 'grandparent_process_path', 'hash_md5', 'host', 'host_type', 'operation_type', 'os', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |