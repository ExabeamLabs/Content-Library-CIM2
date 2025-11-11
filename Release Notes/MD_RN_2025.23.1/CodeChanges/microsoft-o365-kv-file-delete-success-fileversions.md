# Code Changes for microsoft-o365-kv-file-delete-success-fileversions (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'domain', 'email_address', 'event_name', 'file_ext', 'file_name', 'file_path', 'file_type', 'object', 'operation', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['COMMAND=({operation}({event_name}[^=]+?))\s+\w+='] |
| edit_regex_field | object |  | ['OBJECT=({file_path}({object}[^=]+?))\s+\w+='] |
| added_regex_field | file_path |  | ['OBJECT=({file_path}({object}[^=]+?))\s+\w+='] |
| added_regex_field | operation |  | ['COMMAND=({operation}({event_name}[^=]+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |