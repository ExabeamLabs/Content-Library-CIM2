# Code Changes for unix-unix-kv-endpoint-activity-fail-integrityfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['audit\[\d+\]:\s*(({event_name}USER_\S+)|({operation_type}\S+))', 'type=(?:({event_name}USER_\S+)|({operation_type}\S+))'] |
| edit_regex_field | operation_type |  | ['audit\[\d+\]:\s*(({event_name}USER_\S+)|({operation_type}\S+))', 'type=(?:({event_name}USER_\S+)|({operation_type}\S+))'] |