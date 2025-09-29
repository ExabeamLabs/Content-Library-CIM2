# Code Changes for unix-unix-str-scheduled-task-start-crond (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'host', 'process_id', 'process_name', 'time', 'user'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |