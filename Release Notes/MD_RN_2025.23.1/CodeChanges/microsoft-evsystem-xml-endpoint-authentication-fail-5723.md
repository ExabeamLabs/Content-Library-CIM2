# Code Changes for microsoft-evsystem-xml-endpoint-authentication-fail-5723 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'event_id', 'event_name', 'failure_reason', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | failure_reason |  | ['<Data>({failure_reason}[^<]+)<', '<Message>({failure_reason}[^<]+?)\s*<'] |
| removed_attribute | DupFields |  | N/A |