# Code Changes for microsoft-evazureadppdca-xml-app-notification-30006 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_code', 'event_name', 'host', 'operation', 'process_id', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}The service is now enforcing the following Azure password policy))'] |
| added_regex_field | operation |  | ['({operation}({event_name}The service is now enforcing the following Azure password policy))'] |
| removed_attribute | DupFields |  | N/A |