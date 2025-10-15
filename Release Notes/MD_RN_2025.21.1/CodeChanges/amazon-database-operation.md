# Code Changes for amazon-database-operation (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_operation', 'db_query', 'db_user', 'table_name', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\):({user}({db_user}[^@]+?))@'] |
| added_regex_field | user |  | ['\):({user}({db_user}[^@]+?))@'] |
| removed_attribute | DupFields |  | N/A |