# Code Changes for postgresql-p-str-database-login-success-authenticated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'auth_method', 'db_name', 'db_operation', 'dest_host', 'host', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s+({host}[\w\-\.]+)\spostgres', '\w+\s\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\-\.]+)\spostgres'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}[\w\-.]+)<'] |