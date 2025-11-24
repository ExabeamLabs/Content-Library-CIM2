# Code Changes for microsoft-evsecurity-xml-app-authentication-1200 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'email_address', 'endpoint', 'error_code', 'event_code', 'event_id', 'event_name', 'failure_reason', 'host', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'result', 'run_level', 'server', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_agent', 'user_sid'] |
| edit_regex_field | event_name |  | ['<Message>({operation}({event_name}[^:<\.]+))', '<Message>({operation}({event_name}[^<]+?))\.(\s|<)'] |
| added_regex_field | operation |  | ['<Message>({operation}({event_name}[^:<\.]+))', '<Message>({operation}({event_name}[^<]+?))\.(\s|<)'] |