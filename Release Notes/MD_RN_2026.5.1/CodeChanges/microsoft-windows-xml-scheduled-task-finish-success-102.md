# Code Changes for microsoft-windows-xml-scheduled-task-finish-success-102 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'host', 'result', 'run_level', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |