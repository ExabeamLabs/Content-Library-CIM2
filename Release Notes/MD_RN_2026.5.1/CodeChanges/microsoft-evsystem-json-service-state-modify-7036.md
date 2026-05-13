# Code Changes for microsoft-evsystem-json-service-state-modify-7036 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'process_id', 'result', 'service_name', 'service_state', 'time'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |