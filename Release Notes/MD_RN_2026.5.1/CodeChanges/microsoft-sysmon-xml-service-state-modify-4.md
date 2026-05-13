# Code Changes for microsoft-sysmon-xml-service-state-modify-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'event_name', 'host', 'log_name', 'result', 'run_level', 'service_state', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |