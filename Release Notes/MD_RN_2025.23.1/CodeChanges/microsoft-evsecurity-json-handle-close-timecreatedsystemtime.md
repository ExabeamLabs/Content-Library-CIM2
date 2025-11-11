# Code Changes for microsoft-evsecurity-json-handle-close-timecreatedsystemtime (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_id', 'object_server', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(?i)\w+ \d+ \d\d:\d\d:\d\d (am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s'] |
| added_regex_field | dest_host |  | ['(?i)\w+ \d+ \d\d:\d\d:\d\d (am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s'] |
| removed_attribute | DupFields |  | N/A |