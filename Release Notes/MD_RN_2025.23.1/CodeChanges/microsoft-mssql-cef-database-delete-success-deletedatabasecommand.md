# Code Changes for microsoft-mssql-cef-database-delete-success-deletedatabasecommand (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_name', 'db_operation', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'operation', 'time', 'user'] |
| edit_regex_field | event_code |  | ['({host}[\w.\-]+)\s+CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({operation}({event_name}[^\|]+))'] |
| edit_regex_field | event_name |  | ['({host}[\w.\-]+)\s+CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({operation}({event_name}[^\|]+))'] |
| edit_regex_field | host |  | ['({host}[\w.\-]+)\s+CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({operation}({event_name}[^\|]+))'] |
| added_regex_field | operation |  | ['({host}[\w.\-]+)\s+CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({operation}({event_name}[^\|]+))'] |
| removed_attribute | DupFields |  | N/A |