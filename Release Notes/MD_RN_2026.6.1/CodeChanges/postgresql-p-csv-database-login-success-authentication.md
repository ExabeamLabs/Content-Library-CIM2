# Code Changes for postgresql-p-csv-database-login-success-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'db_name', 'db_user', 'dest_host', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s+({host}[\w\-\.]+)\spostgres', '\w+\s\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[\w\-\.]+)\spostgres'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}[\w\-.]+)<'] |