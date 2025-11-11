# Code Changes for microsoft-mssql-xml-database-login-qualifiers (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | db_name |  | ['<Provider Name=(\'|")({db_name}[^\'"]+)(\'|")', 'database_name:({db_name}[^\s:\+]+)'] |