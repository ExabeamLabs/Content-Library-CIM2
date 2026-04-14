# Code Changes for microsoft-evsecurity-xml-configuration-load-4826-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |