# Code Changes for postgresql-p-str-database-activity-context (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'db_name', 'db_operation', 'db_query', 'operation', 'process_id', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))'] |
| added_regex_field | action |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))'] |
| added_regex_field | db_operation |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))'] |
| removed_attribute | DupFields |  | N/A |