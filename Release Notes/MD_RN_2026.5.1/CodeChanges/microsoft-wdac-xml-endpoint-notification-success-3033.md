# Code Changes for microsoft-wdac-xml-endpoint-notification-success-3033 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'host', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'task_name', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |