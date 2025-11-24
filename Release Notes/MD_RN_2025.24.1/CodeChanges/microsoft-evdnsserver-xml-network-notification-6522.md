# Code Changes for microsoft-evdnsserver-xml-network-notification-6522 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_id', 'event_name', 'host', 'operation', 'process_guid', 'process_id', 'run_level', 'time', 'user_sid'] |
| edit_regex_field | event_name |  | ["EventData Name='({operation}({event_name}[^>']+))"] |
| added_regex_field | operation |  | ["EventData Name='({operation}({event_name}[^>']+))"] |