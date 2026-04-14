# Code Changes for microsoft-evsecurity-xml-endpoint-start-4608-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_id', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |