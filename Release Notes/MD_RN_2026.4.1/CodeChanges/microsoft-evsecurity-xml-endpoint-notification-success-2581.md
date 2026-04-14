# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-2581 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'task_name', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |