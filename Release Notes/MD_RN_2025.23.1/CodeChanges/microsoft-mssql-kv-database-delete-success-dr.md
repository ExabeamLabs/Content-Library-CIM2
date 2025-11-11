# Code Changes for microsoft-mssql-kv-database-delete-success-dr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_name', 'db_object', 'db_operation', 'db_query', 'db_schema', 'db_user', 'domain', 'host', 'time', 'user'] |
| edit_regex_field | domain |  | ['\.server_principal_name="*(({domain}[^\\]+?)[\\]{1,2})?({db_user}[^\s]+?)"*(\s+\.sql\.)', '\.server_principal_name="*(({domain}[^\\]+?)[\\]{1,2})?({user}[\w\.\-]{1,40}\$?)"*(\s+\.sql\.)'] |
| added_regex_field | user |  | ['\.server_principal_name="*(({domain}[^\\]+?)[\\]{1,2})?({user}[\w\.\-]{1,40}\$?)"*(\s+\.sql\.)'] |
| removed_attribute | DupFields |  | N/A |