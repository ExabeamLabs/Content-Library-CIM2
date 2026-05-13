# Code Changes for s-mssql-database-login (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'db_name', 'db_user', 'db_user_sid', 'dest_host', 'domain', 'event_code', 'failure_reason', 'host', 'result', 'run_level', 'service_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<', 'Channel="({channel}[^"]+)'] |