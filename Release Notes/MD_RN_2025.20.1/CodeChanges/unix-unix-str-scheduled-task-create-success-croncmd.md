# Code Changes for unix-unix-str-scheduled-task-create-success-croncmd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['host', 'process_command_line', 'process_id', 'process_name', 'process_path', 'task_name', 'user'] |
| edit_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*', '\sCMD\s\(([\w\-]+\s)?({process_path}(\/[^\/\)\s]+?)+?[\/]({process_name}[^\/\)\s]+?))(\s|\))'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |