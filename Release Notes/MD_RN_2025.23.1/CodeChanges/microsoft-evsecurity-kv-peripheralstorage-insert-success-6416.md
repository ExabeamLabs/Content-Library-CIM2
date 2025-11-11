# Code Changes for microsoft-evsecurity-kv-peripheralstorage-insert-success-6416 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'device_class', 'device_description', 'device_id', 'domain', 'event_code', 'event_name', 'operation', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}A new external device was recognized by the system))', 'exa_regex=({operation}({event_name}A new external device was recognized by the system))'] |
| added_regex_field | operation |  | ['({operation}({event_name}A new external device was recognized by the system))', 'exa_regex=({operation}({event_name}A new external device was recognized by the system))'] |
| removed_attribute | DupFields |  | N/A |