# Code Changes for microsoft-mssql-xml-database-query-success-33205-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'db_domain', 'db_name', 'db_operation', 'db_query', 'db_user', 'dest_host', 'domain', 'event_code', 'host', 'result', 'run_level', 'schema_name', 'service_name', 'src_domain', 'src_ip', 'src_port', 'src_user', 'table_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |