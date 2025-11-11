# Code Changes for microsoft-evapp-xml-endpoint-notification-4896 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_hash', 'file_name', 'file_path', 'host', 'process_id', 'provider_name', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+?))<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+?))<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |