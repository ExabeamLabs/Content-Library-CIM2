# Code Changes for microsoft-evapp-xml-endpoint-activity-perflib (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['<Message>({operation}({event_name}[^:<\.]+))', '<Message>({operation}({event_name}[^<]+?))\.(\s|<)'] |
| added_regex_field | operation |  | ['<Message>({operation}({event_name}[^:<\.]+))', '<Message>({operation}({event_name}[^<]+?))\.(\s|<)'] |