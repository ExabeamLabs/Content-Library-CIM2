# Code Changes for microsoft-windows-xml-scheduled-task-trigger-success-200 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'host', 'result', 'result_code', 'run_level', 'task_name', 'time'] |
| added_regex_field | channel |  | ['channel="({channel}[^"]+)'] |