# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-1108 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |