# Code Changes for netapp-n-xml-file-delete-success-4660 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'object_id', 'object_server', 'operation', 'process_dir', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['<EventName>({operation}({event_name}[^<]+))<\/EventName>'] |
| added_regex_field | operation |  | ['<EventName>({operation}({event_name}[^<]+))<\/EventName>'] |
| removed_attribute | DupFields |  | N/A |