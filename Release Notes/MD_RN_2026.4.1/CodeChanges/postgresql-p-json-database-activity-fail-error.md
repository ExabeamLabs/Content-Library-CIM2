# Code Changes for postgresql-p-json-database-activity-fail-error (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_name', 'host', 'operation', 'operation_type', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | host |  | ['\s*(::ffff:)?({host}[^\s]+)?\s*vmdir'] |