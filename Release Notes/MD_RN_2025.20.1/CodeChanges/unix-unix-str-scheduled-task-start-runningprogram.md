# Code Changes for unix-unix-str-scheduled-task-start-runningprogram (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_id', 'event_name', 'host', 'process_id', 'process_name', 'src_ip', 'src_port', 'task_name', 'time'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |