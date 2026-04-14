# Code Changes for microsoft-evsystem-xml-endpoint-notification-success-2004 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'host', 'process_id', 'process_name', 'provider_name', 'result', 'run_level', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |