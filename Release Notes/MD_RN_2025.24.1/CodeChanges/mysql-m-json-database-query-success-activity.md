# Code Changes for mysql-m-json-database-query-success-activity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'db_name', 'db_object', 'db_operation', 'db_query', 'db_user', 'dest_host', 'dest_ip', 'dest_port', 'host', 'os', 'process_id', 'response_size', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['"host":"({host}({dest_host}[^"]+))"'] |
| added_regex_field | host |  | ['"host":"({host}({dest_host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |