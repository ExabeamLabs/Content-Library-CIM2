# Code Changes for microsoft-evsecurity-xml-scheduled-task-create-success-4698-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'arg', 'description', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'run_level', 'task_name', 'time', 'user'] |
| edit_regex_field | host |  | ['\WComputer=({dest_host}({host}[\w\.\-]+))'] |
| added_regex_field | dest_host |  | ['\WComputer=({dest_host}({host}[\w\.\-]+))'] |
| removed_attribute | DupFields |  | N/A |