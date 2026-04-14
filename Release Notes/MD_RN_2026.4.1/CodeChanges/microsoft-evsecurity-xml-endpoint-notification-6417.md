# Code Changes for microsoft-evsecurity-xml-endpoint-notification-6417 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'run_level', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |