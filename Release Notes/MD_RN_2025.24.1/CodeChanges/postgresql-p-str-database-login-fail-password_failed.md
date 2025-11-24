# Code Changes for postgresql-p-str-database-login-fail-password_failed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'db_name', 'db_operation', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))', '({db_operation}({action}({operation}password authentication failed)))'] |
| added_regex_field | action |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))', '({db_operation}({action}({operation}password authentication failed)))'] |
| added_regex_field | db_operation |  | ['(LOG|FATAL):\s*({db_operation}({action}({operation}[^:]+)))', '({db_operation}({action}({operation}password authentication failed)))'] |
| removed_attribute | DupFields |  | N/A |