# Code Changes for microsoft-evsecurity-xml-service-create-success-4622 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'dest_host', 'event_code', 'event_id', 'event_name', 'host', 'operation', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'service_name', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |