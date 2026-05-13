# Code Changes for microsoft-mssql-xml-database-login-qualifiers (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'auth_package', 'channel', 'db_name', 'db_operation', 'db_query', 'db_schema', 'db_user', 'dest_host', 'domain', 'event_code', 'host', 'result', 'result_reason', 'run_level', 'src_host', 'src_ip', 'src_port', 'table_name', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |