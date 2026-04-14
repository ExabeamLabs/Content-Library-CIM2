# Code Changes for microsoft-evsystem-xml-endpoint-notification-success-5807 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'host', 'run_level', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |