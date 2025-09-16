# Code Changes for microsoft-evsystem-json-service-state-modify-7036 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'process_id', 'result', 'service_name', 'service_state', 'time'] |
| added_regex_field | service_name |  | ['The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state'] |
| added_regex_field | service_state |  | ['The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state'] |