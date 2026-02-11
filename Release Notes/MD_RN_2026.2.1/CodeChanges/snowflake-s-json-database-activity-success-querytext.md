# Code Changes for snowflake-s-json-database-activity-success-querytext (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | db_operation |  | ['exa_json_path=$.QUERY_TEXT,exa_regex=({db_operation}(?i)(insert|delete|truncate|drop|alter|create|update|enable|disable|merge|select|dbcc))', 'exa_json_path=$.QUERY_TYPE,exa_regex=({db_operation}[^"]+)'] |