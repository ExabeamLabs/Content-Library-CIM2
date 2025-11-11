# Code Changes for microsoft-mssql-json-database-activity-success-dbactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_name', 'db_object', 'db_operation', 'db_query', 'db_schema', 'db_user', 'domain', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | domain |  | ['"server_principal_name":\s*"(({domain}[^\\"]+?)[\\]{1,2})?({db_user}[^\s"]+?)"', '"server_principal_name":\s*"(({domain}[^\\"]+?)[\\]{1,2})?({user}[\w\.\-]{1,40}\$?)"'] |
| added_regex_field | user |  | ['"server_principal_name":\s*"(({domain}[^\\"]+?)[\\]{1,2})?({user}[\w\.\-]{1,40}\$?)"'] |
| removed_attribute | DupFields |  | N/A |