# Code Changes for microsoft-evsecurity-cef-scheduled-task-modify-4702 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'task_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"(?:winlog\.)?computer_name":"({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['"(?:winlog\.)?computer_name":"({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |