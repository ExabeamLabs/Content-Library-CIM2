# Code Changes for microsoft-evsystem-str-service-state-modify-7040 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'service_name', 'service_state', 'time'] |
| edit_regex_field | service_name |  | ['The start type of the ({service_name}.+?)\sservice', 'The start type of the ({service_name}[^\.="]+) service was changed from[^\.="]+ to ({service_state}[^\.="]+)'] |
| added_regex_field | service_state |  | ['The start type of the ({service_name}[^\.="]+) service was changed from[^\.="]+ to ({service_state}[^\.="]+)'] |