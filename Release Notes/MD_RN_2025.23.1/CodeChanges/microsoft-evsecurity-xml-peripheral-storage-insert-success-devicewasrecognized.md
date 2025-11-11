# Code Changes for microsoft-evsecurity-xml-peripheral-storage-insert-success-devicewasrecognized (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'device_class', 'device_description', 'device_id', 'device_name', 'device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'host', 'operation', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}A new external device was recognized by the system))'] |
| added_regex_field | operation |  | ['({operation}({event_name}A new external device was recognized by the system))'] |
| removed_attribute | DupFields |  | N/A |