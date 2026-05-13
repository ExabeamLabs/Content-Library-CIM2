# Code Changes for microsoft-sysmon-xml-endpoint-notification-success-255 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'host', 'log_name', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |