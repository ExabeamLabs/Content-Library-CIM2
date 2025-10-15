# Code Changes for oracle-db-kv-database-query-success-select (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'db_name', 'db_object', 'db_operation', 'db_query', 'db_schema', 'db_user', 'host', 'return_code', 'time', 'user'] |
| edit_regex_field | account |  | ['sql\.DB_USER=({db_user}({account}[^=]+?))\s+[\w\.]+?='] |
| added_regex_field | db_user |  | ['sql\.DB_USER=({db_user}({account}[^=]+?))\s+[\w\.]+?='] |
| removed_attribute | DupFields |  | N/A |