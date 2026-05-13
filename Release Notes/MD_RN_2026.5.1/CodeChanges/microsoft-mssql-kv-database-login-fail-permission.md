# Code Changes for microsoft-mssql-kv-database-login-fail-permission (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'db_name', 'db_operation', 'db_user', 'dest_host', 'domain', 'event_name', 'failure_reason', 'host', 'session_id', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |