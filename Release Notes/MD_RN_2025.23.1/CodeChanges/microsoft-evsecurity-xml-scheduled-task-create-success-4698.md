# Code Changes for microsoft-evsecurity-xml-scheduled-task-create-success-4698 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'arg', 'author', 'description', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type_text', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'task_name', 'time', 'triggers', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | dest_host |  | ['Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |