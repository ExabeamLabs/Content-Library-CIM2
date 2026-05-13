# Code Changes for microsoft-windows-xml-app-activity-success-10036 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'task', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |