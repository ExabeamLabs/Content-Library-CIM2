# Code Changes for microsoft-m365auditlogs-kv-file-unshare-sharingrevoked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'domain', 'email_address', 'event_name', 'file_ext', 'file_name', 'file_type', 'object', 'operation', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['COMMAND=({operation}({event_name}[^=]+?))\s+\w+='] |
| added_regex_field | operation |  | ['COMMAND=({operation}({event_name}[^=]+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |