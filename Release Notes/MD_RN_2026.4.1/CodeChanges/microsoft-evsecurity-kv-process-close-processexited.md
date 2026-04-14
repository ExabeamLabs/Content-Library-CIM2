# Code Changes for microsoft-evsecurity-kv-process-close-processexited (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'auth_package', 'auth_process', 'channel', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'login_id', 'login_type', 'object', 'object_class', 'operation_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |