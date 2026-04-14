# Code Changes for microsoft-evsecurity-xml-dll-load-4614 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'object', 'process_id', 'result', 'run_level', 'src_host', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |