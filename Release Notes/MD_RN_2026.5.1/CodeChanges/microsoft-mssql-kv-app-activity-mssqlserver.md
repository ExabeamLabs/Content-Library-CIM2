# Code Changes for microsoft-mssql-kv-app-activity-mssqlserver (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'db_name', 'db_operation', 'db_query', 'db_schema', 'db_user', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'host', 'object', 'object_id', 'session_id', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |