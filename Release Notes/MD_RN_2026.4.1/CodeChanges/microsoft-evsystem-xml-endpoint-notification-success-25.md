# Code Changes for microsoft-evsystem-xml-endpoint-notification-success-25 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_id', 'event_name', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |