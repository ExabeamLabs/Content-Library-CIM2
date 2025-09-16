# Code Changes for microsoft-evsystem-kv-service-state-modify-7040 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'auth_package', 'auth_process', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'login_id', 'login_type', 'object', 'object_class', 'operation_type', 'privileges', 'result', 'run_level', 'service_name', 'service_state', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | service_name |  | ['The start type of the ({service_name}[^\.="]+) service was changed from[^\.="]+ to ({service_state}[^\.="]+)'] |
| added_regex_field | service_state |  | ['The start type of the ({service_name}[^\.="]+) service was changed from[^\.="]+ to ({service_state}[^\.="]+)'] |