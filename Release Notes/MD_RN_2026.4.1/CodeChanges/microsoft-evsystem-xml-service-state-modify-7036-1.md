# Code Changes for microsoft-evsystem-xml-service-state-modify-7036-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'process_id', 'run_level', 'service_name', 'service_state', 'src_host', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |