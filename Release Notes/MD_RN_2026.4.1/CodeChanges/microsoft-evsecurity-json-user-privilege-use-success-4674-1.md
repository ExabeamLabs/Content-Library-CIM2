# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-4674-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'channel', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'object', 'object_server', 'object_type', 'ownership_privilege', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_ip', 'src_port', 'src_user', 'task_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |