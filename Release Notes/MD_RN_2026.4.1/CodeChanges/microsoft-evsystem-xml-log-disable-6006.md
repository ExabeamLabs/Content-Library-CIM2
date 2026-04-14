# Code Changes for microsoft-evsystem-xml-log-disable-6006 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'event_name', 'host', 'process_id', 'provider_name', 'result', 'run_level', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |