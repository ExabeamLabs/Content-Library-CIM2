# Code Changes for microsoft-m365auditlogs-kv-report-read-success-viewreport (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'data_set_name', 'domain', 'email_address', 'event_name', 'file_ext', 'file_name', 'file_type', 'object', 'operation', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['COMMAND=({operation}({event_name}[^=]+?))\s+\w+='] |
| added_regex_field | operation |  | ['COMMAND=({operation}({event_name}[^=]+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |