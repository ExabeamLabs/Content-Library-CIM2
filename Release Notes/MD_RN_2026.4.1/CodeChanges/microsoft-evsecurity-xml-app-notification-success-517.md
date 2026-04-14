# Code Changes for microsoft-evsecurity-xml-app-notification-success-517 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_id', 'event_name', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |