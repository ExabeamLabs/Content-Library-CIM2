# Code Changes for oracle-db-kv-database-login-success-unifiedaudit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_id', 'db_name', 'db_operation', 'db_user', 'host', 'return_code', 'user'] |
| edit_regex_field | db_name |  | ['DBID:\s*"+({db_id}({db_name}\d+))'] |
| added_regex_field | db_id |  | ['DBID:\s*"+({db_id}({db_name}\d+))'] |
| removed_attribute | DupFields |  | N/A |