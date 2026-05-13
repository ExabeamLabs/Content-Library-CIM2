# Code Changes for microsoft-evsecurity-xml-service-create-success-5478-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'dest_host', 'event_id', 'host', 'process_guid', 'process_id', 'result', 'run_level', 'sub_category', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |