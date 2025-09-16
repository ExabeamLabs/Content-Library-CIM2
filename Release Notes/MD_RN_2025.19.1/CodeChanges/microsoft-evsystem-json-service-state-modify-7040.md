# Code Changes for microsoft-evsystem-json-service-state-modify-7040 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'host', 'log_source', 'new_value', 'old_value', 'process_guid', 'process_id', 'service_name', 'service_state', 'time', 'user', 'user_sid', 'user_type'] |
| added_regex_field | service_name |  | ['The start type of the ({service_name}[^\.="]+) service was changed from[^\.="]+ to ({service_state}[^\.="]+)'] |
| added_regex_field | service_state |  | ['The start type of the ({service_name}[^\.="]+) service was changed from[^\.="]+ to ({service_state}[^\.="]+)'] |