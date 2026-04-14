# Code Changes for microsoft-evsecurity-json-user-unlock-success-4767-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'auth_package', 'auth_process', 'channel', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'os', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel\\?"+:\\?"({channel}[^\"]+)'] |