# Code Changes for microsoft-wdac-xml-endpoint-notification-success-3033 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'host', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'task_name', 'thread_id', 'time', 'user_sid'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |