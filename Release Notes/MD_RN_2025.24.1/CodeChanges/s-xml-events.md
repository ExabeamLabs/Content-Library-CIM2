# Code Changes for s-xml-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'event_code', 'event_id', 'event_name', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'task_name', 'thread_id', 'time', 'user_sid'] |
| removed_regex_field | domain |  | [] |
| edit_regex_field | event_name |  | ['<Message>({operation}({event_name}[^:<\.]+))', '<Message>({operation}({event_name}[^<]+?))\.(\s|<)'] |
| removed_regex_field | src_ip |  | [] |
| removed_regex_field | src_port |  | [] |
| removed_regex_field | user |  | [] |
| added_regex_field | operation |  | ['<Message>({operation}({event_name}[^:<\.]+))', '<Message>({operation}({event_name}[^<]+?))\.(\s|<)'] |