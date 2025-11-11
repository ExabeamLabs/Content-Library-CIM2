# Code Changes for microsoft-mssql-xml-database-login-success-33205 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | db_name |  | ['\Wdatabase_name:({db_name}[^\s:\+]+)'] |
| edit_regex_field | dest_host |  | ['server_instance_name:({dest_host}[\w\-.]+)'] |