# Code Changes for postgresql-p-str-database-login-success-authenticated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'auth_method', 'db_name', 'db_operation', 'host', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | method |  | [] |
| added_regex_field | auth_method |  | ['method=({auth_method}[^\s]+)'] |