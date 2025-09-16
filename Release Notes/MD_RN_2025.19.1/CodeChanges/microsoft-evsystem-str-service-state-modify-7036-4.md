# Code Changes for microsoft-evsystem-str-service-state-modify-7036-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'service_name', 'service_state', 'time'] |
| edit_regex_field | service_name |  | ['Information\s+\S+\s+\S+\s+(The )?({service_name}.+?)\sservice ', 'The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state'] |
| added_regex_field | service_state |  | ['The ({service_name}[^\.="]+) service entered the ({service_state}[^\.="]+) state'] |