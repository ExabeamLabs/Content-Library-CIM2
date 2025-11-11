# Code Changes for microsoft-evsecurity-xml-scheduled-task-create-success-4700-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'task_name', 'time', 'user'] |
| edit_regex_field | host |  | ['"Computer":"({dest_host}({host}[^"]+))"', '<Computer>({dest_host}({host}[^<]+?))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))', '\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(::ffff:)?({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['"Computer":"({dest_host}({host}[^"]+))"', '<Computer>({dest_host}({host}[^<]+?))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))', '\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(::ffff:)?({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |