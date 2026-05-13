# Code Changes for microsoft-windows-xml-scheduled-task-finish-success-201 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'host', 'result', 'result_code', 'run_level', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |