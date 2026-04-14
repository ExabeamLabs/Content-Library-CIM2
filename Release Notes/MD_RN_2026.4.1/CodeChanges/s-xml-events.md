# Code Changes for s-xml-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'event_code', 'event_id', 'event_name', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'task_name', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |