# Code Changes for postgresql-parser-str-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'db_name', 'db_operation', 'operation', 'process_id', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))'] |
| added_regex_field | action |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))'] |
| added_regex_field | db_operation |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))'] |
| removed_attribute | DupFields |  | N/A |